<template>
  <section class="program-list-case-study py-5">
    <div class="container">
      <h2 class="text-center mb-4 text-white">Our program</h2>
      <ul class="nav nav-tabs justify-content-center mb-4 border-0" role="tablist">
        <li class="nav-item" v-for="ind in industries" :key="ind" role="presentation">
          <button
            class="nav-link bg-transparent text-uppercase fw-bold"
            :class="{ active: activeTab === ind, 'text-warning': activeTab === ind, 'text-white': activeTab !== ind }"
            @click="activeTab = ind"
            type="button"
            role="tab"
            style="border: none; font-size:1.1rem;"
          >
            {{ ind }}
          </button>
        </li>
      </ul>
      <div class="row align-items-center justify-content-center g-4 flex-column-reverse flex-md-row">
        <div class="col-12 col-md-6 d-flex justify-content-center">
          <img :src="activeProgram?.image" alt="Case Study Image" class="img-fluid rounded-4 shadow-lg w-100" style="max-height:400px; object-fit:cover;" />
        </div>
        <div class="col-12 col-md-6 d-flex justify-content-center">
          <div class="case-card bg-dark bg-opacity-75 text-white rounded-4 p-4 w-100 border border-secondary shadow-lg" style="backdrop-filter: blur(2px);">
            <div class="fw-bold text-uppercase mb-2" style="letter-spacing:1px;">{{ activeProgram?.industry }}</div>
            <div class="mb-3">
              <span v-for="badge in activeProgram?.badges" :key="badge" class="badge rounded-pill border border-light text-white me-2 mb-2" style="background:rgba(255,255,255,0.08);font-size:1rem;">{{ badge }}</span>
            </div>
            <h3 class="fw-bold mb-3">{{ activeProgram?.title }}</h3>
            <div class="mb-3 text-white-50">{{ activeProgram?.desc }}</div>
            <a :href="activeProgram?.link" class="fw-bold text-warning text-decoration-none">Click to Read more <i class="bi bi-arrow-right"></i></a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { ref, computed } from 'vue';
const programs = [
  {
    title: "Transforming User Experience: Telkomsel's Journey to UI/UX Excellence",
    industry: 'Telecommunication',
    desc: 'From insight to innovation: How UI/UX training drives the biggest telco provider in Indonesia',
    image: 'https://images.pexels.com/photos/1181675/pexels-photo-1181675.jpeg',
    badges: ['Capacity Building', 'UI/UX Training'],
    link: '#',
  },
  {
    title: 'Digital Talent Bootcamp',
    industry: 'Finance',
    desc: 'Program CSR BCA & BINAR menghasilkan ratusan talenta digital siap kerja, alumni terserap industri dalam 2-3 bulan.',
    image: 'https://images.pexels.com/photos/3184301/pexels-photo-3184301.jpeg',
    badges: ['Capacity Building', 'Digital Bootcamp'],
    link: '#',
  },
  {
    title: 'Transformasi Digital Pemerintah',
    industry: 'Government',
    desc: 'Pelatihan dan workshop AI untuk 100.000 ASN, kolaborasi dengan Microsoft dan Kementerian Kominfo.',
    image: 'https://images.pexels.com/photos/1181406/pexels-photo-1181406.jpeg',
    badges: ['Capacity Building', 'AI Training'],
    link: '#',
  },
  {
    title: 'Data Training Bootcamp',
    industry: 'Manufacture',
    desc: 'Karyawan Danone menguasai otomasi data dan reporting B2B lebih cepat dan akurat setelah bootcamp intensif.',
    image: 'https://images.pexels.com/photos/256369/pexels-photo-256369.jpeg',
    badges: ['Capacity Building', 'Data Training'],
    link: '#',
  },
  {
    title: 'Digital Business Mini Masters',
    industry: 'Education',
    desc: 'Program eksekutif bersama LM FEB UI, membekali pemimpin dengan strategi digital masa depan.',
    image: 'https://images.pexels.com/photos/1181671/pexels-photo-1181671.jpeg',
    badges: ['Executive Education', 'Digital Training'],
    link: '#',
  },
  {
    title: 'Tech Talent Solutions',
    industry: 'Tech Talent',
    desc: 'Solusi rekrutmen dan penempatan talenta IT terbaik untuk akselerasi transformasi digital perusahaan.',
    image: 'https://images.pexels.com/photos/1181672/pexels-photo-1181672.jpeg',
    badges: ['Tech Talent'],
    link: '#',
  },
];
const industries = programs.map(p => p.industry);
const activeTab = ref(industries[0]);
const activeProgram = computed(() => programs.find(p => p.industry === activeTab.value));
</script>

<style scoped>
.nav-tabs .nav-link.active {
  color: #ffc107 !important;
  border: none;
  background: rgba(255,255,255,0.08);
  box-shadow: 0 2px 16px rgba(255,193,7,0.08);
}
.nav-tabs .nav-link {
  border: none;
  background: transparent;
  color: #fff;
  margin: 0 0.5rem;
  transition: color 0.2s;
}
.case-card {
  min-height: 340px;
}
section {
  background-color: #000 !important;
}
</style>
<!-- Pastikan Bootstrap Icons sudah diimport di index.html atau main.ts --> 