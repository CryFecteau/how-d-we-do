<template>
  <cardComponent>
    <form>
      <h2>rate us on a scale of 1-10</h2>
      <ratingSelectComponent :rating="rating" @updateRating="updateRating" />
      <div class="input-group">
        <label for="name">Name</label>
        <input type="text" id="name" placeholder="review" />
        <button type="submit" :disabled="btnDisabled">Submit</button>
      </div>
      <div class="meaage">BLah blah blah</div>
    </form>
  </cardComponent>
</template>
<script setup>
import { ref } from "vue";
import cardComponent from "./shared/card.component.vue";
import ratingSelectComponent from "./ratingSelect.component.vue";
const text = ref("");
const btnDisabled = ref(false);
const message = ref("");
const rating = ref(5);
const updateRating = (newVal) => {
  rating.value = newVal;
  console.log(newVal);
};
</script>
