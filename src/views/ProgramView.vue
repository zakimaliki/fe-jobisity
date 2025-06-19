<template>
  <div>
    <HeaderSection />
    <div class="programs-page">
      <h1 class="programs-title">Programs</h1>
      <p class="programs-desc">
        Ikuti program peningkatan kemampuan profesional secara komprehensif dan pembelajaran intensif bersama mentor melalui kelas-kelas short bootcamp.
      </p>
      <div class="programs-grid">
        <ProgramCard
        />
      </div>
    </div>
    <FooterSection />
  </div>
</template>

<script setup lang="ts">
import HeaderSection from '../components/HeaderSection.vue'
import FooterSection from '../components/FooterSection.vue'
import ProgramCard from '../components/ProgramCard.vue'
</script>

<style scoped>
.programs-page {
  max-width: 1100px;
  margin: 0 auto;
  padding: 40px 16px 60px 16px;
  text-align: center;
}
.programs-title {
  font-size: 2.2rem;
  font-weight: 700;
  text-align: center;
  margin-bottom: 0.5rem;
}
.programs-desc {
  text-align: center;
  color: #666;
  font-size: 1.1rem;
  margin-bottom: 2rem;
}
.programs-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(320px, 1fr));
  gap: 32px;
  margin-top: 2.5rem;
  margin-bottom: 2.5rem;
}
@media (max-width: 900px) {
  .programs-grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}
</style> 