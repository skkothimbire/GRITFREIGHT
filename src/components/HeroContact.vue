<script setup>
import heroImageUrl from '@/img/hero.png'; 
</script>
<template>
     <!-- Hero Section -->
    <div 
      class="hero-section d-flex align-items-center"
      :style="{ backgroundImage: `linear-gradient(to bottom, rgba(0,0,0,0.45), rgba(0,0,0,0.45)), url(${heroImageUrl})` }"
    >
    </div>
</template>
<style>
/* --- Hero Section --- */
.hero-section {
  width: 100%;
  min-height: 60vh;
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

</style>