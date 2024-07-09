<script>
export default {
  name: "AppSearch",
};
</script>

<template>
  <div class="p-5">
    <select class="filter" name="filter" id="filter">
      <option value="">select filter...</option>
    </select>
  </div>
</template>

<style lang="scss" scoped>
.filter {
  border-radius: 5px;
  padding: 10px;
}
</style>
