<script setup>
import { RouterLink } from 'vue-router';
import heroImageUrl from '@/img/services_hero.png'; 
</script>

<template>
  <div class="hero-container">

   

    <!-- Hero Section -->
    <div 
      class="hero-section d-flex align-items-center"
      :style="{ backgroundImage: `linear-gradient(to bottom, rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url(${heroImageUrl})` }"
    >
      <div class="container text-center text-lg-start">
        <div class="row align-items-center">
          <div class="col-lg-7 hero-text">
            <h1 class="display-3 mb-4">Gritfreight: On Time, Every Time.</h1>
            <p class="mb-4">Your reliable partner for comprehensive sea, land, and air logistics solutions across the globe.</p>
            <RouterLink to="/about" class="btn btn-primary btn-lg me-3">Our Services</RouterLink>
            <RouterLink to="/quote" class="btn btn-outline-light btn-lg">Get a Quote</RouterLink>
          </div>
        </div>
      </div>
    </div>

  </div>
</template>

<style scoped>
:root {
  --bs-primary: #f8c146;
}

/* --- Navbar --- */
.custom-navbar {
  background-color: rgba(0,0,0,0.3);
  position: fixed;
  width: 100%;
  z-index: 1030;
  transition: background-color 0.4s ease;
}

.custom-navbar.scrolled {
  background-color: rgba(0,0,0,0.85);
}

.custom-navbar .navbar-brand h2 {
  color: #fff;
  font-weight: bold;
  text-shadow: 2px 2px 6px rgba(0,0,0,0.6);
}

.custom-navbar .nav-link {
  color: #fff;
  transition: 0.3s;
}

.custom-navbar .nav-link:hover,
.custom-navbar .nav-link.active {
  color: var(--bs-primary);
}

/* --- Hero Section --- */
.hero-section {
  width: 100%;
  min-height: 100vh;
  background-size: cover;
  background-position: center;
  position: relative;
  display: flex;
  align-items: center;
}

.hero-text h1 {
  color: #fff;
  text-shadow: 3px 3px 15px rgba(0,0,0,0.7);
  font-weight: bold;
}

.hero-text p {
  color: #fff;
  font-size: 1.2rem;
  text-shadow: 2px 2px 10px rgba(0,0,0,0.6);
}

/* Buttons */
.btn-primary {
  transition: 0.3s;
}
.btn-primary:hover {
  background-color: #fff;
  color: var(--bs-primary);
}

.btn-outline-light {
  transition: 0.3s;
}
.btn-outline-light:hover {
  background-color: var(--bs-primary);
  border-color: var(--bs-primary);
  color: #000;
}

/* Responsive */
@media (max-width: 991.98px) {
  .hero-text {
    text-align: center;
    margin-top: 80px;
  }
  .custom-navbar {
    background-color: rgba(0,0,0,0.95) !important;
  }
}
</style>
