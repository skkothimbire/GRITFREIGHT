<script setup>
import NavBar from '@/components/NavBar.vue';
import Hero from '@/components/Hero.vue';
import AboutSection from '@/components/AboutSection.vue';
import ServicesCards from '@/components/ServicesCards.vue';
import Footer from '@/components/Footer.vue';
import WhyChooseUS from '@/components/WhyChooseUS.vue';
</script>

<template>
  <div class="homepage">

    <!-- Navbar -->
    <NavBar />

    <!-- Hero Section -->
    <Hero />

    <!-- About Section -->
    <section class="section-spacing bg-light about-section">
      <div class="container text-center">
        <h2 class="section-title mb-4">About Us</h2>
        <p class="section-subtitle mb-5">
          Learn more about who we are, what we do, and why Gritfreight is your trusted logistics partner.
        </p>
        <AboutSection />
      </div>
    </section>

    <!-- Services Section -->
    <section class="section-spacing services-section">
      <div class="container text-center">
        <h2 class="section-title mb-4">Our Services</h2>
        <p class="section-subtitle mb-5">
          Explore our wide range of logistics and transportation solutions designed to meet global demands.
        </p>
        <ServicesCards />
      </div>
    </section>
    <WhyChooseUS />

    <!-- Call to Action -->
    <!-- <section class="cta-section d-flex align-items-center justify-content-center text-center text-white">
      <div class="overlay"></div>
      <div class="container position-relative z-2">
        <h2 class="fw-bold mb-3">Ready to Ship with Confidence?</h2>
        <p class="lead mb-4">Let’s move your business forward with seamless, efficient, and reliable logistics.</p>
        <RouterLink to="/contact" class="btn btn-primary px-4 py-2">Get in Touch</RouterLink>
      </div>
    </section> -->

    <!-- Footer -->
    <Footer />

  </div>
</template>

<style scoped>
/* --- General Layout --- */
.section-spacing {
  padding: 80px 0;
}

.section-title {
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 1px;
  color: #222;
  position: relative;
  display: inline-block;
}

.section-title::after {
  content: "";
  position: absolute;
  bottom: -10px;
  left: 50%;
  width: 60px;
  height: 3px;
  background: var(--bs-primary);
  transform: translateX(-50%);
}

.section-subtitle {
  max-width: 700px;
  margin: 0 auto;
  color: #555;
  font-size: 1.1rem;
}

/* --- CTA Section --- */
.cta-section {
  background: url('@/img/cta_bg.jpg') center/cover no-repeat;
  height: 60vh;
  position: relative;
  overflow: hidden;
}

.cta-section .overlay {
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.6);
}

.cta-section h2 {
  font-size: 2.5rem;
  text-shadow: 2px 2px 8px rgba(0,0,0,0.5);
}

.cta-section p {
  font-size: 1.2rem;
  color: #ddd;
}

/* --- Responsive --- */
@media (max-width: 992px) {
  .section-spacing {
    padding: 60px 20px;
  }
  .cta-section {
    height: auto;
    padding: 60px 20px;
  }
  .cta-section h2 {
    font-size: 2rem;
  }
  .cta-section p {
    font-size: 1rem;
  }
}

@media (max-width: 576px) {
  .section-title {
    font-size: 1.6rem;
  }
  .section-subtitle {
    font-size: 1rem;
  }
}
</style>
