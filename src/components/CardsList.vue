<script>
import AppCards from "./AppCards.vue";

export default {
  name: "CardsList",
  components: {
    AppCards,
  },
};
</script>

<template>
  <div class="card-list mx-5 p-5">
    <div class="row">
      <div class="col-12 col-md-4 col-lg-2 mb-2">
        <!-- inserimento cards -->
      </div>
    </div>
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
