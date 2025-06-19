<template>
  <div class="why-jobisity__item program-card" v-for="(program, idx) in programs.slice(0, 3)" :key="idx">
    <div v-if="program.image" class="program-image-wrapper">
      <img :src="program.image" :alt="program.title" class="program-image" loading="lazy" />
    </div>
    <h3 class="why-jobisity__item-title program-title">{{ program.title }}</h3>
    <p class="why-jobisity__item-desc program-description">{{ program.description }}</p>
    <div class="program-actions">
      <button class="btn btn-outline-primary px-4 py-2">Lihat Detail</button>
      <button class="btn btn-primary px-4 py-2">Daftar Sekarang</button>
    </div>
  </div>
</template>

<script setup lang="ts">
import jsImg from '@/assets/js.png'
import devopsImg from '@/assets/devops.png'
import mobileImg from '@/assets/mobile.png'

const programs = [
  {
    title: 'Fullstack Javascript',
    description: 'Belajar coding dengan kurikulum fullstack Javascript, mulai dari frontend hingga backend, siap kerja di industri digital.',
    image: jsImg,
  },
  {
    title: 'DevOps Engineer',
    description: 'Pelajari praktik DevOps modern, CI/CD, cloud, dan automasi untuk menjadi engineer yang dicari perusahaan teknologi.',
    image: devopsImg,
  },
  {
    title: 'Mobile Developer',
    description: 'Bangun aplikasi mobile Android/iOS dengan teknologi terbaru, mulai dari desain hingga deployment ke store.',
    image: mobileImg,
  },
]
</script>

<style scoped>
.why-jobisity__item.program-card {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  background: #fff;
  border-radius: 18px;
  padding: 2.2rem 2rem 2.2rem 2rem;
  box-shadow: 0 4px 24px rgba(20,186,176,0.10);
  border: 1.5px solid #e0e0e0;
  transition: box-shadow 0.2s, transform 0.2s, border-color 0.2s;
  max-width: 420px;
  width: 100%;
  min-width: 320px;
}
.why-jobisity__item.program-card:hover {
  box-shadow: 0 8px 32px rgba(20,186,176,0.18);
  transform: translateY(-6px) scale(1.025);
  border-color: #14bab0;
}
.program-image-wrapper {
  width: 100%;
  max-width: 160px;
  aspect-ratio: 1/1;
  background: linear-gradient(135deg, #eaf1ff 0%, #f7faff 100%);
  border-radius: 1.2rem;
  box-shadow: 0 2px 12px rgba(45,124,255,0.08);
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 1.1rem;
}
.program-image {
  width: 100%;
  height: 100%;
  object-fit: contain;
  object-position: center;
  border-radius: 1.2rem;
  transition: transform 0.3s cubic-bezier(.4,2,.6,1), box-shadow 0.3s;
}
.program-image:hover {
  transform: scale(1.04);
  box-shadow: 0 8px 32px rgba(45,124,255,0.18);
}
.why-jobisity__icon {
  color: #ff6b35;
  background: #fff6f0;
  border-radius: 8px;
  width: 56px;
  height: 56px;
  display: flex;
  align-items: center;
  justify-content: center;
  font-size: 2rem;
  margin-bottom: 1rem;
}
.why-jobisity__item-title.program-title {
  font-size: 1.25rem;
  font-weight: 700;
  margin-bottom: 0.2rem;
  color: #222;
}
.why-jobisity__item-desc.program-description {
  color: #666;
  font-size: 1rem;
  line-height: 1.5;
  margin-bottom: 16px;
}
.program-actions {
  display: flex;
  gap: 12px;
  width: 100%;
  justify-content: center;
  margin-top: 10px;
}
@media (max-width: 600px) {
  .why-jobisity__item.program-card {
    max-width: 98vw;
    min-width: unset;
    padding: 1.2rem 0.5rem 1.2rem 0.5rem;
  }
  .program-image-wrapper {
    max-width: 90px;
    border-radius: 0.7rem;
  }
  .program-image {
    border-radius: 0.7rem;
  }
}
</style> 