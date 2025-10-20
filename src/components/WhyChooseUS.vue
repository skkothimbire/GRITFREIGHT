<template>
  <!-- Why Choose Us Section -->
  <section class="why-choose-us py-5">
    <div class="container">
      <!-- Heading -->
      <div class="text-center mb-5">
        <h6 class="text-primary text-uppercase fw-bold">Why Choose Us</h6>
        <h2 class="fw-bold display-6">Trusted by Businesses Worldwide</h2>
        <p class="text-muted mt-2 mb-0">
          Discover why companies around the globe trust Gritfreight Logistics for reliable, fast, and efficient delivery.
        </p>
      </div>

      <!-- Cards -->
      <div class="row g-4">
        <div
          v-for="(item, index) in features"
          :key="index"
          class="col-lg-3 col-md-6"
        >
          <div
            class="feature-card p-4 h-100 text-center shadow-sm rounded-4 position-relative overflow-hidden"
          >
            <div class="icon-wrapper mx-auto mb-3">
              <i :class="item.icon"></i>
            </div>
            <h5 class="fw-bold mb-3">{{ item.title }}</h5>
            <p class="text-muted small mb-0">{{ item.description }}</p>

            <!-- Decorative gradient line -->
            <div class="feature-border"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    title: "Fastest and On-Time Delivery",
    description:
      "Experience a seamless logistics process with our optimized routes, real-time tracking, and guaranteed delivery timelines.",
    icon: "fa fa-shipping-fast",
  },
  {
    title: "24/7 Customer Support",
    description:
      "Our dedicated support team is available round-the-clock to resolve your queries and ensure complete satisfaction.",
    icon: "fa fa-headset",
  },
  {
    title: "Global Presence",
    description:
      "With our worldwide network, we provide logistics solutions that reach every corner of the globe, efficiently and reliably.",
    icon: "fa fa-globe",
  },
  {
    title: "30+ Years of Experience",
    description:
      "Backed by over three decades of industry expertise, we’ve built a reputation for trust, quality, and reliability.",
    icon: "fa fa-medal",
  },
];
</script>

<style scoped>
.why-choose-us {
  background-color: #f8f9fa;
  padding-top: 80px;
  padding-bottom: 80px;
}

/* Section Heading */
.why-choose-us h6 {
  color: #0d6efd; /* Primary Blue */
  letter-spacing: 1px;
}

.why-choose-us h2 {
  color: #1c1c1c;
}

/* Feature Cards */
.feature-card {
  border: 1px solid #e8e8e8;
  background: #fff;
  transition: all 0.4s ease;
}

.feature-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 20px 45px rgba(0, 0, 0, 0.08);
  border-color: #0d6efd;
}

/* Icon Circle */
.icon-wrapper {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  background: linear-gradient(135deg, #0d6efd1a, #f8c14633);
  display: flex;
  align-items: center;
  justify-content: center;
  transition: all 0.4s ease;
}

.icon-wrapper i {
  font-size: 28px;
  color: #0d6efd;
  transition: all 0.4s ease;
}

.feature-card:hover .icon-wrapper {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
}

.feature-card:hover i {
  color: #fff;
}

/* Decorative border line */
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

/* Responsive */
@media (max-width: 991.98px) {
  .feature-card {
    text-align: center;
  }

  .icon-wrapper {
    margin: 0 auto 15px auto;
  }
}
</style>
