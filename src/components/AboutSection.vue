<template>
  <!-- About Section -->
  <section class="about-section py-5">
    <div class="container">
      <div class="row align-items-center g-5">
        <!-- Left Image -->
        <div
          class="col-lg-6 animate__animated animate__fadeInLeft"
          data-wow-delay="0.1s"
        >
          <div class="about-img-wrapper rounded-4 overflow-hidden position-relative">
            <img
              src="/src/img/about.jpg"
              alt="About Gritfreight Logistics"
              class="img-fluid about-img"
            />
            <div class="about-border"></div>
          </div>
        </div>

        <!-- Right Content -->
        <div
          class="col-lg-6 animate__animated animate__fadeInRight"
          data-wow-delay="0.3s"
        >
          <h6 class="text-primary text-uppercase fw-bold mb-3">
            About Gritfreight
          </h6>
          <h2 class="fw-bold display-6 mb-4">
            Delivering Trust, Speed & Global Reach
          </h2>
          <p class="text-muted mb-4">
            At <strong>Gritfreight Logistics</strong>, we provide
            world-class transportation and logistics solutions across the globe.
            With a strong fleet and expert team, we ensure reliability,
            precision, and on-time delivery for every shipment.
          </p>

          <div class="row g-4 mb-4">
            <div
              v-for="(feature, index) in features"
              :key="index"
              class="col-sm-6"
            >
              <div
                class="about-card d-flex align-items-start text-start p-4 rounded-4 h-100"
              >
                <div class="icon-wrapper me-3 flex-shrink-0">
                  <i :class="feature.icon"></i>
                </div>
                <div>
                  <h5 class="fw-bold mb-2">{{ feature.title }}</h5>
                  <p class="text-muted small mb-0">{{ feature.description }}</p>
                </div>
                <div class="feature-border"></div>
              </div>
            </div>
          </div>

          <RouterLink
            to="/services"
            class="btn about-btn px-4 py-2 rounded-pill fw-semibold shadow-sm"
          >
            Learn More
          </RouterLink>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    title: "Global Coverage",
    description: "Connecting your cargo to major trade routes and ports worldwide.",
    icon: "fa fa-globe",
  },
  {
    title: "On-Time Delivery",
    description: "Precision and reliability are at the heart of our service.",
    icon: "fa fa-shipping-fast",
  },
];
</script>

<style scoped>
.about-section {
  background-color: #f8f9fa;
}

/* === Image Wrapper (With Gradient Line) === */
.about-img-wrapper {
  border: 1px solid #e8e8e8;
  transition: all 0.4s ease;
  overflow: hidden;
  position: relative;
}
.about-img {
  width: 100%;
  height: 370px;
  object-fit: cover;
  transition: transform 0.5s ease, filter 0.4s ease;
}
.about-img-wrapper:hover {
  transform: translateY(-4px);
  box-shadow: 0 20px 45px rgba(0, 0, 0, 0.08);
  border-color: #0d6efd;
}
.about-img-wrapper:hover .about-img {
  transform: scale(1.03);
  filter: brightness(1.05);
}

/* Gradient border animation */
.about-border {
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 0%;
  height: 4px;
  background: linear-gradient(90deg, #0d6efd, #f8c146);
  border-radius: 10px;
  transition: all 0.4s ease;
  transform: translateX(-50%);
}
.about-img-wrapper:hover .about-border {
  width: 80%;
}

/* === Feature Cards (Same as Why Choose Us) === */
.about-card {
  border: 1px solid #e8e8e8;
  background: #fff;
  position: relative;
  transition: all 0.4s ease;
}
.about-card:hover {
  transform: translateY(-8px);
  border-color: #0d6efd;
  box-shadow: 0 20px 45px rgba(0, 0, 0, 0.08);
}

/* Icon */
.icon-wrapper {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: linear-gradient(135deg, #0d6efd1a, #f8c14633);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.4s ease;
}
.icon-wrapper i {
  font-size: 24px;
  color: #0d6efd;
  transition: all 0.4s ease;
}
.about-card:hover .icon-wrapper {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
}
.about-card:hover .icon-wrapper i {
  color: #fff;
}

/* Decorative gradient line on hover */
.feature-border {
  position: absolute;
  bottom: 0;
  left: 50%;
  width: 0%;
  height: 4px;
  background: linear-gradient(90deg, #0d6efd, #f8c146);
  border-radius: 10px;
  transition: all 0.4s ease;
  transform: translateX(-50%);
}
.about-card:hover .feature-border {
  width: 80%;
}

/* === Button Style (Same Gradient Glow) === */
.about-btn {
  background: linear-gradient(90deg, #0d6efd, #0748b1);
  color: #fff;
  border: none;
  transition: all 0.3s ease;
}
.about-btn:hover {
  background: linear-gradient(90deg, #f8c146, #f5b700);
  color: #212529;
  transform: translateY(-2px);
  box-shadow: 0 6px 25px rgba(248, 193, 70, 0.4);
}

/* === Responsive Design === */
@media (max-width: 991.98px) {
  .about-img {
    height: 300px;
  }
  .about-card {
    padding: 1rem;
  }
  .about-section h2 {
    font-size: 1.8rem;
  }
}
</style>
