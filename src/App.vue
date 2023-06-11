<script setup>
import { RouterView } from "vue-router";
import headerComponent from "./components/header.component.vue";
</script>

<template>
  <div>
    <headerComponent />
    <RouterView />
  </div>
</template>

<style scoped></style>
