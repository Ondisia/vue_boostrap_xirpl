<template>
  <!-- Hero -->
  <section class="py-5 text-center bg-light">
    <div class="container">
      <h1 class="fw-bold">Contact Us</h1>
      <p class="lead text-muted">
        Silakan hubungi saya melalui form atau informasi kontak di bawah.
      </p>
    </div>
  </section>

  <!-- Contact Section -->
  <section class="py-5">
    <div class="container">
      <div class="row g-4">
        <!-- Contact Info -->
        <div class="col-lg-5">
          <h3 class="fw-bold mb-4">Informasi Kontak</h3>
          <div class="contact-info mb-3 d-flex align-items-center">
            <i class="bi bi-geo-alt-fill"></i>
            <span>Jl. Contoh No. 123, Jakarta, Indonesia</span>
          </div>
          <div class="contact-info mb-3 d-flex align-items-center">
            <i class="bi bi-envelope-fill"></i>
            <span>email@contoh.com</span>
          </div>
          <div class="contact-info mb-3 d-flex align-items-center">
            <i class="bi bi-telephone-fill"></i>
            <span>+62 812 3456 7890</span>
          </div>
          <div class="contact-info mb-3 d-flex align-items-center">
            <i class="bi bi-globe"></i>
            <span>www.portfolioanda.com</span>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="col-lg-7">
          <div class="card shadow-sm border-0">
            <div class="card-body p-4">
              <h3 class="fw-bold mb-4">Kirim Pesan</h3>
              <form>
                <div class="mb-3">
                  <label for="name" class="form-label">Nama Lengkap</label>
                  <input
                    type="text"
                    class="form-control"
                    id="name"
                    placeholder="Masukkan nama Anda"
                    required
                  />
                </div>
                <div class="mb-3">
                  <label for="email" class="form-label">Email</label>
                  <input
                    type="email"
                    class="form-control"
                    id="email"
                    placeholder="nama@email.com"
                    required
                  />
                </div>
                <div class="mb-3">
                  <label for="message" class="form-label">Pesan</label>
                  <textarea
                    class="form-control"
                    id="message"
                    rows="5"
                    placeholder="Tulis pesan Anda..."
                    required
                  ></textarea>
                </div>
                <button type="submit" class="btn btn-primary px-4">
                  Kirim
                </button>
              </form>
            </div>
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
.contact-info i {
  font-size: 1.5rem;
  margin-right: 10px;
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
