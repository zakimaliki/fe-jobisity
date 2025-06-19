<template>
  <footer class="footer bg-light border-top pt-4 mt-5">
    <div class="container">
      <div class="row gy-4 align-items-start">
        <div class="col-md-4 d-flex flex-column align-items-md-start align-items-center text-md-start text-center mb-4 mb-md-0">
          <img src="@/assets/footer logo.png" alt="Jobisity Footer Logo" class="footer__logo mb-2" />
          <div class="footer__contact mb-2">
            <div>halo@jobisity.com</div>
            <div>(021) 8067 5787</div>
          </div>
          <div class="footer__socials d-flex gap-2 justify-content-md-start justify-content-center">
            <span>IG</span>
            <span>FB</span>
            <span>TW</span>
            <span>YT</span>
          </div>
        </div>
        <div class="col-md-8">
          <div class="row">
            <div class="col-12 col-md-4 mb-3 mb-md-0">
              <div class="footer__col-title mb-2">Our Program</div>
              <ul class="list-group list-group-flush">
                <li class="px-0 py-1 border-0">Fullstack Javascript</li>
                <li class="px-0 py-1 border-0">DevOps Engineer</li>
                <li class="px-0 py-1 border-0">Mobile Developer</li>
              </ul>
            </div>
            <div class="col-12 col-md-4 mb-3 mb-md-0">
              <div class="footer__col-title mb-2">Location</div>
              <ul class="list-group list-group-flush">
                <li class="px-0 py-1 border-0">Jakarta</li>
                <li class="px-0 py-1 border-0">Bandung</li>
                <li class="px-0 py-1 border-0">Tangerang</li>
                <li class="px-0 py-1 border-0">Yogyakarta</li>
                <li class="px-0 py-1 border-0">Surabaya</li>
              </ul>
            </div>
            <div class="col-12 col-md-4">
              <div class="footer__col-title mb-2">Our Service</div>
              <ul class="list-group list-group-flush">
                <li class="px-0 py-1 border-0">Belajar Intensif</li>
                <li class="px-0 py-1 border-0">Growth Mindset</li>
                <li class="px-0 py-1 border-0">Hiring Partners</li>
              </ul>
            </div>
          </div>
        </div>
      </div>
      <div class="footer__bottom text-center py-3 mt-4 text-secondary small">
        <span>&copy; 2025 PT Lumbung Mandiri Bersama. All Rights Reserved</span>
      </div>
    </div>
  </footer>
</template>

<script setup lang="ts">
</script>

<style scoped>
.footer {
  background-color: #000 !important;
  color: #fff;
}
.footer__logo {
  height: 40px;
}
.footer__brand-title {
  font-size: 2rem;
  font-weight: 700;
}
.footer__col-title {
  font-weight: 600;
}
.footer ul,
.footer li {
  list-style: none;
  padding-left: 0;
  margin-left: 0;
}
</style> 