<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <div class="card text-bg-dark">
    <img src="/img/bg.jpg" class="card-img" alt="..." />
    <div class="card-img-overlay">
      <h5 class="card-title">
        <RouterLink class="btn btn-warning" to="/about">About Me</RouterLink>
      </h5>
    </div>
  </div>
</template>

<style scoped>
img {
    height: 90.2vh;
    object-fit: cover;
    object-position: top;
}
h5 {
  position: absolute;
  bottom: 95px;
  left: 47%;
  transform: translateX(-50%);
}
.card {
  border: none;
  border-radius: 0;
}
</style>
