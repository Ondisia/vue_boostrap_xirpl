<script setup>
import { RouterView } from "vue-router";
import NavbarKu from "./components/NavbarKu.vue";
</script>

<template>
  <NavbarKu/>

  <RouterView />

    <!-- Footer -->
  <footer>
    <div class="container">
      <p class="mb-0">&copy; 2025 Nama Anda. All rights reserved.</p>
    </div>
  </footer>
</template>

<style scoped>
footer {
  padding: 20px 0;
  background: #212529;
  color: #fff;
  text-align: center;
}
</style>


<!-- <RouterLink to="/">Home</RouterLink> -->
