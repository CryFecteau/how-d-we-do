<template>
  <ul>
    <li v-for="n in 10" :key="`rating-${n}`">
      <input
        type="radio"
        name="rating"
        :value="n"
        :id="`num${n}`"
        :checked="selectedRating === n"
        v-model="selectedRating"
      />
      <label :for="`num${n}`">{{ n }}</label>
    </li>
  </ul>
</template>

<script>
export default {
  name: "ratingSelectComponent",
  data() {
    return {
      selectedRating: this.rating,
    };
  },
  props: {
    rating: {
      type: Number,
      default: 0,
    },
  },
  watch: {
    selectedRating(newVal) {
      this.$emit("updateRating", newVal);
    },
    rating(newVal) {
      this.selectedRating = newVal;
    },
  },
};
</script>
