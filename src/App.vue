<script>
import AppHeader from "./components/AppHeader.vue";
import AppSearch from "./components/AppSearch.vue";

export default {
  name: "App",
  components: {
    AppHeader,
    AppSearch,
  },
};
</script>

<template>
  <header>
    <AppHeader />
  </header>
  <main>
    <AppSearch />
  </main>
</template>

<style lang="scss">
@use "./style/general.scss";

main {
  background-color: lightsalmon;
}
</style>
