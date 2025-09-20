<script setup>
import { ref, onMounted } from "vue"

const about = ref(null)

onMounted(async () => {
  try {
    const res = await fetch("http://localhost:8000/crud_php_api.php")
    const json = await res.json()
    console.log("API Response:", json) // debug
    if (json.status === "success" && Array.isArray(json.data) && json.data.length > 0) {
      about.value = json.data[0]  // ✅ ambil dari field "data"
    } else {
      console.warn("Data kosong:", json)
    }
  } catch (error) {
    console.error("Gagal ambil data:", error)
  }
})
</script>


<template>
  <!-- About Me Section -->
<section class="py-5" v-if="about">
  <div class="container">
    <div class="row align-items-center">
      <div class="col-lg-6 mb-4 mb-lg-0">
        <img
          :src="`http://localhost:8000/${about.foto}`"
          alt="About Me"
          class="img-fluid rounded shadow"
        />
      </div>
      <div class="col-lg-6">
        <h2 class="fw-bold mb-3">Tentang Saya</h2>
        <p class="text-muted" v-if="about.deskripsi">{{ about.deskripsi }}</p>
        <a
          v-if="about.file_resume"
          :href="`http://localhost:8000/${about.file_resume}`"
          class="btn btn-primary mt-3"
          target="_blank"
        >
          Download CV
        </a>
      </div>
    </div>
  </div>
</section>

<section v-else class="py-5 text-center">
  <p>Loading data...</p>
</section>


  <!-- Skills Section -->
  <section class="py-5 bg-light">
    <div class="container">
      <h2 class="fw-bold text-center mb-5">Keahlian</h2>
      <div class="row text-center">
        <div class="col-md-4 mb-4">
          <div class="p-4 border rounded shadow-sm h-100">
            <h5 class="fw-bold">Frontend</h5>
            <p class="text-muted">HTML, CSS, JavaScript, Bootstrap, React</p>
          </div>
        </div>
        <div class="col-md-4 mb-4">
          <div class="p-4 border rounded shadow-sm h-100">
            <h5 class="fw-bold">Backend</h5>
            <p class="text-muted">Django, Laravel, Node.js, REST API</p>
          </div>
        </div>
        <div class="col-md-4 mb-4">
          <div class="p-4 border rounded shadow-sm h-100">
            <h5 class="fw-bold">Tools</h5>
            <p class="text-muted">Git, Docker, Linux, MySQL, PostgreSQL</p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
body {
  font-family: "Poppins", sans-serif;
  background-color: #f8f9fa;
}
.profile-img {
  max-width: 180px;
  border-radius: 50%;
  height: 200px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15);
}
.social-icons a {
  margin: 0 10px;
  font-size: 1.2rem;
  color: #495057;
  transition: color 0.3s ease;
}
.social-icons a:hover {
  color: #0d6efd;
}
</style>
