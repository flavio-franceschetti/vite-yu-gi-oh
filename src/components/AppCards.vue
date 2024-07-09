<script>
export default {
  name: "AppCards",
  props: ["cardInfo"],
};
</script>

<template>
  <div class="card border-5" style="width: 18rem">
    <img
      :src="cardInfo.card_images[0].image_url"
      class="card-img-top"
      :alt="cardInfo.name"
    />
    <div class="card-body">
      <h5 class="card-title text-white text-uppercase fw-bold">
        {{ cardInfo.name }}
      </h5>
      <p class="card-text">
        {{ cardInfo.archetype }}
      </p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  background-color: lightsalmon;

  img {
    object-fit: cover;
  }
}
</style>
