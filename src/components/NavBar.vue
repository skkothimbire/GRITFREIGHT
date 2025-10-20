<script setup>
import { RouterLink } from 'vue-router';
import { onMounted, onUnmounted } from 'vue';

// Navbar scroll effect & auto-collapse mobile menu
onMounted(() => {
  const navbar = document.querySelector('.custom-navbar');
  const navbarCollapse = document.getElementById('navbarCollapse');
  const navLinks = document.querySelectorAll('.navbar-nav .nav-link');

  // Scroll effect
  const handleScroll = () => {
    if (window.scrollY > 60) navbar.classList.add('scrolled');
    else navbar.classList.remove('scrolled');
  };
  window.addEventListener('scroll', handleScroll);

  // Collapse mobile menu on link click
  navLinks.forEach(link => {
    link.addEventListener('click', () => {
      if (navbarCollapse.classList.contains('show')) {
        const bsCollapse = bootstrap.Collapse.getInstance(navbarCollapse);
        if (bsCollapse) bsCollapse.hide();
      }
    });
  });

  onUnmounted(() => window.removeEventListener('scroll', handleScroll));
});
</script>

<template>
  <div class="hero-container">
    <!-- Navbar -->
    <nav class="navbar navbar-expand-lg custom-navbar">
      <div class="container-fluid px-4 px-lg-5">
        <!-- Brand -->
        <RouterLink to="/" class="navbar-brand d-flex align-items-center">
          <h2 class="brand-title mb-0">GRITFREIGHT</h2>
        </RouterLink>

        <!-- Toggler -->
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarCollapse"
          aria-controls="navbarCollapse"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>

        <!-- Menu -->
        <div class="collapse navbar-collapse" id="navbarCollapse">
          <div class="navbar-nav ms-auto align-items-center gap-3">
            <RouterLink to="/" class="nav-item nav-link">HOME</RouterLink>
            <RouterLink to="/about" class="nav-item nav-link">ABOUT</RouterLink>
            <RouterLink to="/services" class="nav-item nav-link">SERVICES</RouterLink>

            <div class="nav-item dropdown">
              <a href="#" class="nav-link dropdown-toggle" data-bs-toggle="dropdown">PAGES</a>
              <div class="dropdown-menu dropdown-menu-end shadow-sm border-0 rounded-3">
                <RouterLink to="/pricing" class="dropdown-item">Pricing Plan</RouterLink>
                <RouterLink to="/features" class="dropdown-item">Features</RouterLink>
                <RouterLink to="/quote" class="dropdown-item">Free Quote</RouterLink>
                <RouterLink to="/team" class="dropdown-item">Our Team</RouterLink>
                <RouterLink to="/testimonial" class="dropdown-item">Testimonial</RouterLink>
                <RouterLink to="/404" class="dropdown-item">404 Page</RouterLink>
              </div>
            </div>

            <RouterLink to="/contact" class="nav-item nav-link">CONTACT</RouterLink>

            <div class="d-none d-lg-block ms-3 contact-info text-white">
              <i class="fa fa-headphones text-primary me-2"></i> +012 345 6789
            </div>
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<style scoped>
:root {
  --bs-primary: #f8c146;
  --nav-font: "Poppins", sans-serif;
}

/* --- NAVBAR --- */
.custom-navbar {
  background-color: rgba(0, 0, 0, 0.3);
  backdrop-filter: blur(10px);
  position: fixed;
  width: 100%;
  z-index: 1030;
  transition: all 0.4s ease;
  padding: 0.8rem 0;
  box-shadow: none;
}

.custom-navbar.scrolled {
  background-color: rgba(0, 0, 0, 0.9);
  box-shadow: 0 3px 10px rgba(0, 0, 0, 0.4);
}

/* --- BRAND NAME HOVER EFFECT --- */
.brand-title {
  font-size: 1.75rem;
  font-weight: 700;
  color: #fff;
  letter-spacing: 1px;
  text-shadow: 2px 2px 6px rgba(0, 0, 0, 0.6);
  transition: all 0.4s ease;
  padding: 0.2rem 0.5rem;
  border-radius: 0.5rem;
}

.brand-title:hover {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  color: #fff;
  transform: translateY(-1px);
}

/* --- MAIN NAV LINKS --- */
.navbar-nav .nav-link {
  font-family: var(--nav-font);
  font-size: 1rem;
  color: #ffffffcc;
  text-transform: capitalize;
  letter-spacing: 0.3px;
  position: relative;
  transition: all 0.4s ease;
}

/* Bottom border for main nav links */
.navbar-nav .nav-link::after {
  content: "";
  position: absolute;
  bottom: -4px;
  left: 0;
  width: 0%;
  height: 2px;
  background: linear-gradient(90deg, #0d6efd, #f8c146);
  border-radius: 5px;
  transition: width 0.4s ease;
}

/* Hover & active effect for main nav links */
.navbar-nav .nav-link:hover,
.navbar-nav .nav-link.router-link-active {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  transform: translateY(-1px);
}

.navbar-nav .nav-link:hover::after,
.navbar-nav .nav-link.router-link-active::after {
  width: 100%;
}

/* --- DROPDOWN MENU --- */
.dropdown-menu {
  background-color: #fff;
  padding: 0.5rem 0;
  border-radius: 0.5rem;
  animation: fadeIn 0.3s ease;
}

/* Dropdown items hover/click gradient */
.dropdown-item {
  font-family: var(--nav-font);
  font-size: 1rem;
  text-transform: capitalize;
  letter-spacing: 0.3px;
  position: relative;
  padding: 0.5rem 1rem;
  border-radius: 0.5rem;
  color: #333;
  transition: all 0.4s ease;
}

/* Bottom border hidden initially */
.dropdown-item::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 10%;
  width: 0%;
  height: 3px;
  background: linear-gradient(90deg, #0d6efd, #f8c146);
  border-radius: 5px;
  transition: width 0.4s ease;
}

/* Show gradient background & bottom border on hover/focus */
.dropdown-item:hover,
.dropdown-item:focus {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  color: #fff;
}

.dropdown-item:hover::after,
.dropdown-item:focus::after {
  width: 80%;
}

/* --- CONTACT INFO --- */
.contact-info {
  font-family: var(--nav-font);
  font-weight: 500;
  font-size: 0.95rem;
  color: #fff;
}

/* --- NAVBAR TOGGLER --- */
.navbar-toggler {
  border: 1px solid rgba(255, 255, 255, 0.7);
}

.navbar-toggler-icon {
  background-image: url("data:image/svg+xml;charset=utf8,%3Csvg viewBox='0 0 30 30' xmlns='http://www.w3.org/2000/svg'%3E%3Cpath stroke='rgba%28255,255,255,1%29' stroke-width='2' stroke-linecap='round' stroke-miterlimit='10' d='M4 7h22M4 15h22M4 23h22'/%3E%3C/svg%3E");
}

/* --- RESPONSIVE --- */
@media (max-width: 991.98px) {
  .custom-navbar {
    background-color: rgba(0, 0, 0, 0.95) !important;
  }

  .navbar-nav {
    text-align: center;
  }

  .nav-item {
    margin: 0.6rem 0;
  }

  .contact-info {
    display: none;
  }
}

/* --- ANIMATION --- */
@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(5px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}


</style>
