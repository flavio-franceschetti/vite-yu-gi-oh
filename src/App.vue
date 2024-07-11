<script>
// importo axios
import axios from "axios";

import AppHeader from "./components/AppHeader.vue";
import AppSearch from "./components/AppSearch.vue";
import CardsList from "./components/CardsList.vue";

// importo store in appvue
import { store } from "./store.js";

export default {
  name: "App",
  components: {
    AppHeader,
    AppSearch,
    CardsList,
  },

  data() {
    return {
      store,
    };
  },
  methods: {
    getCards() {
      let endPoint = store.apiURL;
      store.loading = true;

      // quando viene selezionato l archetipo dal filtro aggiungiamo una richiesta
      if (store.cardFilter !== "") {
        endPoint += `&${store.apiCardArchetype}=${store.cardFilter}`;
      }
      axios
        .get(endPoint)
        .then(function (response) {
          // handle success
          console.log(response.data.data);
          store.cardsList = response.data.data;
          store.loading = false;
        })
        .catch(function (error) {
          // handle error
          console.log(error);
          store.loading = false;
        });
    },

    getArchetype() {
      axios
        .get(store.apiArchetypesURL)
        .then(function (response) {
          // handle success
          store.archetypesList = response.data;
          console.log(response.data);
        })
        .catch(function (error) {
          // handle error
          console.log(error);
        });
    },
  },

  created() {
    this.getArchetype();
    this.getCards();
  },
};
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main class="container-fluid p-4">
    <AppSearch @filter="getCards" />
    <CardsList />
  </main>
</template>

<style lang="scss">
@use "./style/general.scss";

main {
  background-color: lightsalmon;
}
</style>
