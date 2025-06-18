<template>
  <header class="header bg-white border-bottom">
    <nav class="navbar navbar-expand-lg navbar-light bg-white container">
      <a class="navbar-brand d-flex align-items-center" href="#">
        <img src="@/assets/logo.png" alt="Jobisity Logo" class="header__logo me-2" height="40" />
        <span class="fw-bold fs-4">Jobisity</span>
      </a>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav mx-auto mb-2 mb-lg-0 gap-lg-4 gap-2">
          <li class="nav-item"><RouterLink class="nav-link" to="/jobs">Jobs</RouterLink></li>
          <li class="nav-item"><RouterLink class="nav-link" to="/programs">Programs</RouterLink></li>
          <li class="nav-item"><RouterLink class="nav-link" to="/about">About</RouterLink></li>
          <li class="nav-item"><RouterLink class="nav-link" to="/corporate">For Corporate</RouterLink></li>
        </ul>
        <button class="btn btn-outline-primary ms-lg-3 mt-2 mt-lg-0">Konsultasi Gratis</button>
      </div>
    </nav>
  </header>
</template>

<script setup lang="ts">
import { RouterLink } from 'vue-router'
</script>

<style scoped>
.header__logo {
  height: 40px;
}
</style> 