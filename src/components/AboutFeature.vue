<template>
  <!-- Feature Section -->
  <section class="feature-section py-5">
    <div class="container">
      <div class="row g-5 align-items-center">
        <!-- Feature Text -->
        <div class="col-lg-6 animate__animated animate__fadeInUp" data-wow-delay="0.1s">
          <h6 class="text-primary text-uppercase fw-bold mb-3">Our Features</h6>
          <h2 class="fw-bold mb-4">We Are a Trusted Logistics Company Since 1990</h2>
          <p class="text-muted mb-5">
            At Gritfreight Logistics, we ensure seamless transportation and logistics services with precision, safety, and speed.  
            Explore what makes us one of the most trusted names in the industry.
          </p>

          <div
            v-for="(feature, index) in features"
            :key="index"
            class="d-flex align-items-start feature-card p-4 rounded-4 border mb-4 shadow-sm position-relative overflow-hidden"
            :style="{ animationDelay: feature.delay }"
          >
            <div class="icon-box flex-shrink-0 me-3">
              <i :class="feature.icon"></i>
            </div>
            <div>
              <h5 class="fw-bold mb-2">{{ feature.title }}</h5>
              <p class="text-muted small mb-0">{{ feature.description }}</p>
            </div>

            <div class="feature-border"></div>
          </div>
        </div>

        <!-- Feature Image -->
        <div class="col-lg-6 animate__animated animate__fadeInRight" data-wow-delay="0.1s">
          <div class="feature-img-wrapper rounded-4 overflow-hidden shadow-lg position-relative">
            <img
              src="/src/img/feature.jpg"
              alt="Features Image"
              class="img-fluid w-100 h-100"
              style="object-fit: cover;"
            />
            <div class="overlay-gradient"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    title: "Worldwide Service",
    description:
      "We provide reliable logistics services across the globe, connecting your business to all major trade routes and destinations.",
    icon: "fa fa-globe",
    delay: "0.2s",
  },
  {
    title: "On-Time Delivery",
    description:
      "Precision and punctuality are our priorities. Our expert planning ensures every shipment arrives exactly when it should.",
    icon: "fa fa-shipping-fast",
    delay: "0.4s",
  },
  {
    title: "24/7 Support",
    description:
      "Our dedicated support team is available 24/7 to assist you, ensuring seamless logistics experiences without delays.",
    icon: "fa fa-headset",
    delay: "0.6s",
  },
];
</script>

<style scoped>
.feature-section {
  background-color: #f8f9fa;
  padding-top: 80px;
  padding-bottom: 80px;
}

/* Headings */
.feature-section h6 {
  color: #0d6efd;
  letter-spacing: 1px;
}

.feature-section h2 {
  color: #1c1c1c;
  line-height: 1.4;
}

/* Feature Card */
.feature-card {
  border: 1px solid #e8e8e8;
  background: #fff;
  transition: all 0.4s ease;
  cursor: pointer;
}
.feature-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 15px 35px rgba(0, 0, 0, 0.08);
  border-color: #0d6efd;
}

/* Icon Box */
.icon-box {
  width: 60px;
  height: 60px;
  border-radius: 50%;
  background: linear-gradient(135deg, #0d6efd1a, #f8c14633);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.4s ease;
}
.icon-box i {
  font-size: 22px;
  color: #0d6efd;
  transition: all 0.4s ease;
}
.feature-card:hover .icon-box {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
}
.feature-card:hover .icon-box i {
  color: #fff;
}

/* Decorative border */
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
.feature-card:hover .feature-border {
  width: 80%;
}

/* Feature Image */
.feature-img-wrapper img {
  transition: transform 0.6s ease, box-shadow 0.5s ease;
}
.feature-img-wrapper img:hover {
  transform: scale(1.05);
}
.overlay-gradient {
  position: absolute;
  bottom: 0;
  width: 100%;
  height: 40%;
  background: linear-gradient(180deg, transparent, rgba(0, 0, 0, 0.2));
  border-bottom-left-radius: 1rem;
  border-bottom-right-radius: 1rem;
}

/* Responsive */
@media (max-width: 991.98px) {
  .feature-section h2 {
    font-size: 1.8rem;
  }

  .icon-box {
    width: 50px;
    height: 50px;
  }

  .icon-box i {
    font-size: 20px;
  }
}
</style>
