<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <div class="d-flex align-items-center gap-3 header container-fluid">
    <div class="header-logo">
      <img src="../assets/img/logo yu-gi-oh.png" alt="logo yu-gi-oh" />
    </div>
    <h1 class="mb-0">Yu-Gi-Oh Api</h1>
  </div>
</template>

<style lang="scss" scoped>
.header {
  height: 50px;
  h1 {
    font-size: 30px;
  }

  .header-logo {
    width: 100px;
  }
}
</style>
