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
      axios
        .get(store.apiURL)
        .then(function (response) {
          // handle success
          console.log(response.data.data);
          store.cardsList = response.data.data;
          store.loading = false;
        })
        .catch(function (error) {
          // handle error
          console.log(error);
        });
    },
  },
  created() {
    this.getCards();
  },
};
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main class="container-fluid p-4">
    <AppSearch />
    <CardsList />
  </main>
</template>

<style lang="scss">
@use "./style/general.scss";

main {
  background-color: lightsalmon;
}
</style>
