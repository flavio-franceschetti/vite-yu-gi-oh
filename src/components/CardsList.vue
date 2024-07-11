<script>
import AppCards from "./AppCards.vue";
import AppLoader from "./AppLoader.vue";
import { store } from "../store.js";

export default {
  name: "CardsList",
  components: {
    AppCards,
    AppLoader,
  },

  data() {
    return {
      store,
    };
  },

  computed: {
    cardresult() {
      return store.cardsList.length;
    },
  },
};
</script>

<template>
  <div class="card-list mx-5 p-5">
    <div class="p-3 mb-2 bg-dark text-white">
      Carte trovate {{ cardresult }}
    </div>
    <div v-if="!store.loading" class="row">
      <div
        v-for="(card, index) in store.cardsList"
        :key="index"
        class="col-12 col-md-4 col-lg-2 mb-2 mx-4"
      >
        <!-- inserimento cards -->
        <AppCards :cardInfo="card" />
      </div>
    </div>
    <AppLoader v-else />
  </div>
</template>

<style lang="scss" scoped>
.card-list {
  background-color: #fff;
}
.prova {
  width: 100%;
  height: 100px;
  background-color: black;
}
</style>
