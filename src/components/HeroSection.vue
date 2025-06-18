<template>
  <section class="hero bg-white py-5">
    <div class="container">
      <div class="row align-items-center justify-content-center">
        <div class="col-md-6 mb-4 mb-md-0 d-flex flex-column align-items-md-start align-items-center text-md-start text-center">
          <h1 class="hero__title mb-3">Bangun Karier Impianmu Bersama <span>Jobisity</span></h1>
          <p class="hero__desc mb-4">
            Temukan program pelatihan terbaik, konsultasi gratis, dan dukungan penuh untuk mengembangkan potensi serta meraih pekerjaan impian. Mulai perjalanan suksesmu bersama kami!
          </p>
          <div class="d-flex gap-3 flex-wrap justify-content-md-start justify-content-center">
            <button class="btn btn-primary px-4 py-2">Pendaftaran</button>
            <button class="btn btn-outline-primary px-4 py-2">Konsultasi Gratis</button>
          </div>
        </div>
        <div class="col-md-6 d-flex justify-content-center">
          <slot name="image">
            <div class="hero__img-placeholder d-flex align-items-center justify-content-center">
              <svg width="80" height="80" viewBox="0 0 24 24" fill="none" stroke="#bbb" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="3" y="3" width="18" height="18" rx="4"/><path d="M3 17l6-6a2 2 0 0 1 2.8 0l7.2 7"/><circle cx="9" cy="9" r="2"/></svg>
            </div>
          </slot>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
</script>

<style scoped>
.hero__title {
  font-size: 2.6rem;
  font-weight: 800;
  line-height: 1.15;
}
.hero__title span {
  color: #2d7cff;
}
.hero__desc {
  font-size: 1.18rem;
  color: #222;
  line-height: 1.6;
}
.hero__img-placeholder {
  width: 280px;
  height: 280px;
  border: 2.5px dashed #bbb;
  background: #f7faff;
  border-radius: 18px;
  box-shadow: 0 2px 12px rgba(45,124,255,0.04);
}
@media (max-width: 900px) {
  .hero__img-placeholder {
    width: 180px;
    height: 180px;
  }
  .hero__title {
    font-size: 1.35rem;
  }
  .hero__desc {
    font-size: 0.98rem;
  }
}
@media (max-width: 600px) {
  .hero__img-placeholder {
    width: 120px;
    height: 120px;
  }
}
</style> 