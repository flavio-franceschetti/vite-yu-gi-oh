<script>
import { store } from "../store.js";

export default {
  name: "AppSearch",

  data() {
    return {
      store,
    };
  },
};
</script>

<template>
  <div class="p-5">
    <select
      v-model="store.cardFilter"
      @change="$emit('filter')"
      name="filter"
      id="filter"
    >
      <option value="">sleziona il tipo...</option>
      <option
        v-for="(archetype, index) in store.archetypesList"
        :key="index"
        :value="archetype.archetype_name"
      >
        {{ archetype.archetype_name }}
      </option>
    </select>
  </div>
</template>

<style lang="scss" scoped>
#filter {
  border-radius: 5px;
  padding: 10px;
}
</style>
