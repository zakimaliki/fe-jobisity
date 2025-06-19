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
            <div class="hero__img-wrapper d-flex align-items-center justify-content-center">
              <img
                :src="heroImg"
                alt="Karier Impianmu Bersama Jobisity"
                class="hero__img"
                loading="lazy"
              />
            </div>
          </slot>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import heroImg from '@/assets/hero.avif';
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
.hero__img-wrapper {
  width: 100%;
  max-width: 540px;
  aspect-ratio: 16/9;
  background: linear-gradient(135deg, #eaf1ff 0%, #f7faff 100%);
  border-radius: 2.5rem;
  box-shadow: 0 8px 32px rgba(45,124,255,0.10), 0 1.5px 8px rgba(45,124,255,0.04);
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
}
.hero__img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
  border-radius: 2.5rem;
  box-shadow: 0 2px 16px rgba(45,124,255,0.08);
  transition: transform 0.3s cubic-bezier(.4,2,.6,1), box-shadow 0.3s;
}
.hero__img:hover {
  transform: scale(1.035);
  box-shadow: 0 8px 32px rgba(45,124,255,0.18);
}
@media (max-width: 1200px) {
  .hero__img-wrapper {
    max-width: 420px;
    border-radius: 2rem;
  }
  .hero__img {
    border-radius: 2rem;
  }
}
@media (max-width: 900px) {
  .hero__img-wrapper {
    max-width: 90vw;
    aspect-ratio: 16/10;
    border-radius: 1.2rem;
  }
  .hero__img {
    border-radius: 1.2rem;
  }
  .hero__title {
    font-size: 1.35rem;
  }
  .hero__desc {
    font-size: 0.98rem;
  }
}
@media (max-width: 600px) {
  .hero__img-wrapper {
    max-width: 98vw;
    aspect-ratio: 16/12;
    border-radius: 0.7rem;
  }
  .hero__img {
    border-radius: 0.7rem;
  }
}
</style> 