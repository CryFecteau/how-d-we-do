<script setup></script>

<template>
  <div class="home-container">
    <div class="home-content">
      <reviewFormComponent />
      <reviewStatsComponent />
      <reviewListComponent />
    </div>
  </div>
</template>

<script setup>
import reviewFormComponent from "../components/reviewForm.component.vue";
import reviewStatsComponent from "../components/reviewStats.component.vue";
import reviewListComponent from "../components/reviewList.component.vue";
</script>
