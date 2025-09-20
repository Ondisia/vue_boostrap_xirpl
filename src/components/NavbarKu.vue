<script setup>
import { RouterLink } from "vue-router";
</script>

<template>
  <nav class="navbar navbar-expand-lg">
    <div class="container-fluid">
      <RouterLink class="navbar-brand" to="/">bLackDomon</RouterLink>

      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav mx-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <RouterLink class="nav-link" to="/" exact-active-class="active"
              ><i class="bi bi-house-fill"></i> Home</RouterLink
            >
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link mx-4" to="/about" exact-active-class="active"
              ><i class="bi bi-person-badge-fill"></i> About</RouterLink
            >
          </li>
          <li class="nav-item">
            <RouterLink class="nav-link" to="/contact" exact-active-class="active"
              ><i class="bi bi-telephone-fill"></i> Contact</RouterLink
            >
          </li>
        </ul>
        <form class="d-flex" role="search">
          <input
            class="form-control me-2"
            type="search"
            placeholder="Search"
            aria-label="Search"
          />
          <button class="btn btn-light" type="submit">Search</button>
        </form>
      </div>
    </div>
  </nav>
</template>


<style scoped>
.navbar {
  background-color: #015778;
}
.navbar-brand {
  color: white;
  font-weight: bold;
  font-size: 25px;
}
.nav-link {
  color: white;
  font-weight: bold;
  font-size: 20px;
  border-radius: 0.5rem;
}
.nav-link.active {
  font-weight: bold;
  color: #0d6efd !important;     /* warna teks */
  background-color: #fff;  /* biru Bootstrap */
  border-radius: 0.5rem;      /* biar agak rounded */
}
.nav-link:hover {
  font-weight: bold;
  color: #0d6efd !important;     /* warna teks */
  background-color: #fff;  /* biru Bootstrap */
  border-radius: 0.5rem;      /* biar agak rounded */
}
</style>