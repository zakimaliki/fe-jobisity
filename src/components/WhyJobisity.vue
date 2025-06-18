<template>
  <section class="why-jobisity bg-white py-5">
    <div class="container">
      <h2 class="text-center mb-2 fw-bold why-jobisity__title">Kenapa Jobisity Menjadi Pelatihan Coding Bootcamp Terbaik</h2>
      <p class="text-center mb-5 why-jobisity__subtitle">Jobisity sudah teruji menghasilkan para lulusan yang kompeten di industri melalui program bootcamp.</p>
      <div class="why-jobisity__grid">
        <div class="why-jobisity__item">
          <span class="why-jobisity__icon"><font-awesome-icon :icon="['fas', 'code']" /></span>
          <div class="why-jobisity__item-title">Belajar Intensif</div>
          <div class="why-jobisity__item-desc">Siswa difokuskan belajar secara intensif dari pukul 09.00 - 18.00 WIB untuk menjadi Full Stack Developer atau Data Scientist.</div>
        </div>
        <div class="why-jobisity__item">
          <span class="why-jobisity__icon"><font-awesome-icon :icon="['fas', 'brain']" /></span>
          <div class="why-jobisity__item-title">Growth Mindset</div>
          <div class="why-jobisity__item-desc">Setiap siswa dibekali dengan growth mindset untuk bisa berkembang di mana pun mereka berkarir.</div>
        </div>
        <div class="why-jobisity__item">
          <span class="why-jobisity__icon"><font-awesome-icon :icon="['fas', 'handshake']" /></span>
          <div class="why-jobisity__item-title">Hiring Partners</div>
          <div class="why-jobisity__item-desc">Kami bekerja sama dengan 750+ perusahaan yang siap merekrut lulusan program bootcamp kami.</div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup lang="ts">
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
</script>

<style scoped>
.why-jobisity {
  padding: 3rem 0 2rem 0;
  text-align: center;
}
.why-jobisity__title {
  font-size: 2.2rem;
}
.why-jobisity__subtitle {
  color: #555;
  font-size: 1.15rem;
}
.why-jobisity__grid {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 2.5rem 2rem;
  max-width: 900px;
  margin: 0 auto;
}
.why-jobisity__item {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  background: #fff;
  border-radius: 18px;
  padding: 2rem 1.2rem 1.7rem 1.2rem;
  box-shadow: 0 4px 24px rgba(20,186,176,0.10);
  border: 1.5px solid #e0e0e0;
  transition: box-shadow 0.2s, transform 0.2s;
}
.why-jobisity__item:hover {
  box-shadow: 0 8px 32px rgba(20,186,176,0.18);
  transform: translateY(-6px) scale(1.025);
  border-color: #14bab0;
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
.why-jobisity__item-title {
  font-size: 1.25rem;
  font-weight: 700;
  margin-bottom: 0.2rem;
  color: #222;
}
.why-jobisity__item-desc {
  color: #666;
  font-size: 1rem;
  line-height: 1.5;
}
@media (max-width: 900px) {
  .why-jobisity__grid {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }
}
</style> 