<template>
  <div class="card-container" :class="{ reverse: reverse }">
    <slot />
  </div>
</template>

<script>
export default {
  name: "CardComponent",
  props: {
    reverse: {
      type: Boolean,
      default: false,
    },
  },
};
</script>

<style scoped>
.card-container {
  background: white;
  color: black;
}
.card-container.reverse {
  background: black;
  color: white;
}
</style>
