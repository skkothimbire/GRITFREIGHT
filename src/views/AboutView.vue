<script setup>
import Footer from '@/components/Footer.vue';
import NavBar from '@/components/NavBar.vue'; 
import { RouterLink } from 'vue-router';
import AboutSection from '@/components/AboutSection.vue';
import AboutFeature from '@/components/AboutFeature.vue';
import AboutOurTeam from '@/components/AboutOurTeam.vue';
import WhyChooseUS from '@/components/WhyChooseUS.vue';
</script>

<template>
  <NavBar />

  <!-- Header Section -->
  <header class="page-header text-center text-white d-flex flex-column justify-content-center align-items-center">
    <div class="container animate__animated animate__fadeInDown">
      <h1 class="display-5 fw-bold mb-3">About Us</h1>
      <nav aria-label="breadcrumb">
        <ol class="breadcrumb justify-content-center mb-0">
          <li class="breadcrumb-item">
            <RouterLink to="/" class="text-white-50 text-decoration-none">Home</RouterLink>
          </li>
          <li class="breadcrumb-item text-white-50">Pages</li>
          <li class="breadcrumb-item active text-white" aria-current="page">
            About
          </li>
        </ol>
      </nav>
    </div>
  </header>
  <!-- About Section -->
  <AboutSection />
  <AboutFeature />
  <WhyChooseUS />
  <AboutOurTeam />
  <Footer />
</template>

<style scoped>
/* --- NAVBAR STYLING --- */
.custom-navbar {
  background-color: transparent;
  transition: background-color 0.4s ease, box-shadow 0.4s ease;
  padding: 1rem 0;
}

.custom-navbar.scrolled {
  background-color: rgba(0, 0, 0, 0.9);
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.4);
}

.navbar-brand {
  letter-spacing: 1px;
}

.navbar-nav .nav-link {
  color: #ffffffcc;
  margin-left: 1rem;
  transition: 0.3s;
}

.navbar-nav .nav-link:hover,
.navbar-nav .nav-link.active {
  color: var(--bs-primary);
}

/* Adjust header spacing */
header {
  margin-top: 0;
}

/* --- HEADER SECTION --- */
.page-header {
  background: linear-gradient(rgba(0, 0, 0, 0.65), rgba(0, 0, 0, 0.65)),
    url('/src/img/about_us_header.png') center/cover no-repeat;
  height: 60vh;
  width: 100%;
  overflow: hidden;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
}

/* --- ABOUT SECTION --- */
.about-section {
  padding: 80px 15px;
  margin-top: 0;
}

.about-section img {
  transition: transform 0.5s ease, box-shadow 0.5s ease;
}

.about-section img:hover {
  transform: scale(1.03);
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.25);
}

/* --- ANIMATION --- */
.about-section {
  animation: fadeUp 0.8s ease-in-out;
}

@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* --- RESPONSIVE DESIGN --- */
@media (max-width: 991.98px) {
  .custom-navbar {
    background-color: rgba(0, 0, 0, 0.95);
  }

  .navbar-nav .nav-link {
    margin: 0.6rem 0;
    text-align: center;
    font-size: 1.1rem;
  }

  .page-header {
    height: 40vh;
  }

  .page-header h1 {
    font-size: 1.8rem;
  }

  .breadcrumb {
    font-size: 0.9rem;
  }
}
</style>

<script>
// Add scroll detection for navbar transparency
window.addEventListener('scroll', () => {
  const navbar = document.querySelector('.custom-navbar');
  if (window.scrollY > 60) {
    navbar.classList.add('scrolled');
  } else {
    navbar.classList.remove('scrolled');
  }
});
</script>
