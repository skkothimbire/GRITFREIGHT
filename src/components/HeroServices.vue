<script setup>
import heroImageUrl from '@/img/hero.png'; 
</script>

<template>
  <!-- Hero Section -->
  <div 
    class="hero-section d-flex align-items-center justify-content-center"
    :style="{ backgroundImage: `linear-gradient(to bottom, rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url(${heroImageUrl})` }"
  >
    <div class="hero-text text-center">
      <h1>Our Services</h1>
      <p>Reliable. Efficient. Professional.</p>
    </div>
  </div>
</template>

<style scoped>
/* --- Hero Section --- */
.hero-section {
  width: 100%;
  min-height: 60vh;
  background-size: cover; /* Ensures full coverage */
  background-position: center center;
  background-repeat: no-repeat;
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  overflow: hidden;
}

/* Better scaling on smaller screens */
@media (max-width: 992px) {
  .hero-section {
    min-height: 50vh;
    background-size: cover;
    background-position: center top; /* Slightly top-aligned for better fit */
  }
}

@media (max-width: 576px) {
  .hero-section {
    min-height: 40vh;
    background-size: contain; /* Show full image on small screens */
    background-position: center;
    background-color: #000; /* fallback background if image doesn't fill space */
  }
}

/* --- Text Styling --- */
.hero-text h1 {
  color: #fff;
  text-shadow: 3px 3px 15px rgba(0,0,0,0.7);
  font-weight: bold;
  font-size: clamp(1.8rem, 4vw, 3rem);
}

.hero-text p {
  color: #fff;
  font-size: clamp(1rem, 2vw, 1.3rem);
  text-shadow: 2px 2px 10px rgba(0,0,0,0.6);
}

/* --- Buttons (if added later) --- */
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
</style>
