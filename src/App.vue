<script>
import AppHeader from "./components/AppHeader.vue";
import AppSearch from "./components/AppSearch.vue";
import CardsList from "./components/CardsList.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppSearch,
    CardsList,
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
