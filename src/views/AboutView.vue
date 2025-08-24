<template>
  <!-- About Me Section -->
  <section class="py-5">
    <div class="container">
      <div class="row align-items-center">
        <div class="col-lg-6 mb-4 mb-lg-0">
          <img
            src="/img/foto.jpg"
            alt="About Me"
            class="img-fluid rounded shadow"
          />
        </div>
        <div class="col-lg-6">
          <h2 class="fw-bold mb-3">Tentang Saya</h2>
          <p class="text-muted">
            Halo! Saya adalah seorang web developer dengan pengalaman dalam
            membangun website modern, responsif, dan user-friendly. Saya
            terbiasa menggunakan framework seperti Django, Laravel, serta
            menguasai frontend dengan Bootstrap dan React.
          </p>
          <p class="text-muted">
            Fokus saya adalah membuat aplikasi yang tidak hanya berfungsi dengan
            baik tetapi juga memiliki desain yang bersih dan profesional. Saya
            juga terus belajar teknologi terbaru untuk selalu update dengan
            perkembangan industri.
          </p>
          <a href="#" class="btn btn-primary mt-3">Download CV</a>
        </div>
      </div>
    </div>
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

  <!-- Footer -->
  <footer>
    <div class="container">
      <p class="mb-0">&copy; 2025 Nama Anda. All rights reserved.</p>
    </div>
  </footer>
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
footer {
  margin-top: 50px;
  padding: 20px 0;
  background: #212529;
  color: #fff;
  text-align: center;
}
</style>
