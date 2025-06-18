<template>
  <section class="testimonial-list py-5">
    <div class="container">
      <h2 class="text-center mb-4">Testimoni</h2>
      <Splide
        :options="splideOptions"
        class="pb-5"
      >
        <SplideSlide v-for="(t, idx) in testimonials" :key="idx">
          <div class="d-flex justify-content-center h-100">
            <div class="card h-100 shadow-sm border-0 align-items-center" style="max-width: 340px;">
              <div class="card-body d-flex flex-column align-items-center text-center">
                <div class="mb-3">
                  <svg xmlns="http://www.w3.org/2000/svg" width="64" height="64" fill="#6c757d" class="bi bi-person-circle" viewBox="0 0 16 16">
                    <path d="M11 10a2 2 0 1 1-4 0 2 2 0 0 1 4 0z"/>
                    <path fill-rule="evenodd" d="M0 8a8 8 0 1 1 16 0A8 8 0 0 1 0 8zm8-7a7 7 0 0 0 0 14A7 7 0 0 0 8 1zM4.285 12.433A5.985 5.985 0 0 1 8 11c1.306 0 2.518.418 3.715 1.433A6.978 6.978 0 0 1 8 13a6.978 6.978 0 0 1-3.715-0.567z"/>
                  </svg>
                </div>
                <div class="fw-bold mb-2">{{ t.name }}</div>
                <div class="fst-italic text-secondary">
                  "{{ t.quote }}"
                </div>
              </div>
            </div>
          </div>
        </SplideSlide>
      </Splide>
    </div>
  </section>
</template>

<script setup lang="ts">
const testimonials = [
  { name: 'John Doe', quote: 'Jobisity membantu saya mendapatkan pekerjaan impian dengan mentor yang sangat suportif dan materi yang relevan dengan industri.' },
  { name: 'Sarah Putri', quote: 'Materi pelatihan di Jobisity sangat aplikatif dan mudah dipahami. Saya jadi lebih percaya diri menghadapi dunia kerja.' },
  { name: 'Budi Santoso', quote: 'Komunitas Jobisity sangat suportif, banyak peluang networking dan konsultasi karier yang membantu perkembangan saya.' },
  { name: 'Rina Kurnia', quote: 'Fasilitas dan dukungan karier di Jobisity sangat membantu saya berkembang.' },
  { name: 'Andi Wijaya', quote: 'Mentor di Jobisity sangat ramah dan profesional.' },
  { name: 'Dewi Lestari', quote: 'Saya mendapat banyak insight baru dan teman baru di komunitas Jobisity.' },
  { name: 'Fajar Pratama', quote: 'Programnya sangat terstruktur dan mudah diikuti.' },
  { name: 'Siti Aminah', quote: 'Jobisity memberikan peluang kerja yang luas dan relevan.' },
  { name: 'Rizky Saputra', quote: 'Saya sangat merekomendasikan Jobisity untuk pengembangan karier.' },
];

const splideOptions = {
  type: 'loop',
  perPage: 3,
  gap: '30px',
  pagination: true,
  arrows: true,
  breakpoints: {
    900: { perPage: 2 },
    600: { perPage: 1 },
  },
};

import { Splide, SplideSlide } from '@splidejs/vue-splide';
import '@splidejs/vue-splide/css';
</script>

<style scoped>
.splide__arrow {
  background: #2d7cff;
  color: #fff;
}
.splide__pagination__page.is-active {
  background: #2d7cff;
}
</style> 