<script>
export default {
  name: "AppLoader",
  props: ["cardInfo"],
};
</script>

<template>
  <div class="loader">
    <iframe
      src="https://giphy.com/embed/sL00sB0pH5oVaQclLc"
      width="480"
      height="269"
      style=""
      frameBorder="0"
      allowFullScreen
    ></iframe>
  </div>
</template>

<style lang="scss" scoped>
.loader {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background-color: #ffffffc1;
  height: 100%;
  width: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>
