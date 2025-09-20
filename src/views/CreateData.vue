<script setup>
import { ref } from "vue"

const form = ref({
  deskripsi: "",
  foto: null,
  file_resume: null,
})

const message = ref("")
const messageClass = ref("alert-info")

// handle file input
function handleFileChange(event, field) {
  form.value[field] = event.target.files[0]
}

// handle submit
async function handleSubmit() {
  try {
    const formData = new FormData()
    formData.append("action", "create") // biar PHP tahu ini create
    formData.append("deskripsi", form.value.deskripsi)
    formData.append("foto", form.value.foto)
    formData.append("file_resume", form.value.file_resume)

    const res = await fetch("http://localhost:8000/crud_php_api.php", {
      method: "POST",
      body: formData,
    })

    const data = await res.json()
    console.log("API Response:", data)

    if (data.status === "success") {
      message.value = "Data berhasil disimpan!"
      messageClass.value = "alert-success"
      // reset form
      form.value.deskripsi = ""
      form.value.foto = null
      form.value.file_resume = null
      document.getElementById("foto").value = ""
      document.getElementById("file_resume").value = ""
    } else {
      message.value = "Gagal menyimpan data: " + (data.message || "")
      messageClass.value = "alert-danger"
    }
  } catch (err) {
    console.error(err)
    message.value = "Terjadi kesalahan koneksi"
    messageClass.value = "alert-danger"
  }
}
</script>
<template>
  <section class="py-5">
    <div class="container">
      <h2 class="fw-bold mb-4">Tambah Aset Website</h2>

      <form @submit.prevent="handleSubmit" enctype="multipart/form-data">
        <!-- Foto -->
        <div class="mb-3">
          <label for="foto" class="form-label">Foto</label>
          <input
            type="file"
            class="form-control"
            id="foto"
            @change="handleFileChange($event, 'foto')"
            accept="image/*"
            required
          />
        </div>

        <!-- Deskripsi -->
        <div class="mb-3">
          <label for="deskripsi" class="form-label">Deskripsi</label>
          <textarea
            id="deskripsi"
            class="form-control"
            v-model="form.deskripsi"
            rows="4"
            required
          ></textarea>
        </div>

        <!-- File Resume -->
        <div class="mb-3">
          <label for="file_resume" class="form-label">File Resume</label>
          <input
            type="file"
            class="form-control"
            id="file_resume"
            @change="handleFileChange($event, 'file_resume')"
            accept=".pdf,.doc,.docx"
            required
          />
        </div>

        <!-- Tombol -->
        <button type="submit" class="btn btn-primary">Simpan</button>
      </form>

      <!-- Pesan sukses / error -->
      <div v-if="message" class="alert mt-3" :class="messageClass">
        {{ message }}
      </div>
    </div>
  </section>
</template>


