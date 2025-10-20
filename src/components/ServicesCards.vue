<template>
  <!-- Services Start -->
  <section class="services-section container-xxl py-5">
    <div class="container text-center mb-5">
      <h6 class="text-primary text-uppercase fw-bold">Our Services</h6>
      <h2 class="fw-bold display-6 mb-3">Reliable Freight & Logistics Solutions</h2>
      <p class="text-muted w-75 mx-auto">
        From air to ocean, road to rail — we move your cargo safely, swiftly, and efficiently across the globe.
      </p>
    </div>


    <div class="container">
      <div class="row g-4">
        <div
          v-for="(service, index) in services"
          :key="index"
          class="col-md-6 col-lg-4 animate__animated animate__fadeInUp"
          :style="{ animationDelay: `${0.2 + index * 0.1}s` }"
        >
          <div class="service-item rounded-4 shadow-sm overflow-hidden">
            <div class="image-wrapper">
              <img :src="service.image" class="img-fluid w-100" :alt="service.title" />
              <div class="image-overlay d-flex align-items-center justify-content-center">
                <RouterLink
                  to="/services"
                  class="btn btn-light text-primary fw-semibold rounded-pill px-3 py-2"
                >
                  <i class="fa fa-arrow-right me-2"></i>Read More
                </RouterLink>
              </div>
            </div>
            <div class="p-4 text-center">
              <h4 class="fw-semibold mb-2">{{ service.title }}</h4>
              <p class="text-muted small mb-0">{{ service.description }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
  <!-- Services End -->
</template>


<script setup>
const services = [
  {
    title: "Air Freight",
    description: "Fast, secure, and efficient global air cargo solutions for all shipment sizes.",
    image: "/src/img/service-1.jpg",
  },
  {
    title: "Ocean Freight",
    description: "Reliable sea freight with global port coverage and cost-effective transit.",
    image: "/src/img/service-2.jpg",
  },
  {
    title: "Road Freight",
    description: "Comprehensive ground transportation with guaranteed delivery timelines.",
    image: "/src/img/service-3.jpg",
  },
  {
    title: "Train Freight",
    description: "Sustainable and efficient rail logistics connecting major industrial routes.",
    image: "/src/img/service-4.jpg",
  },
  {
    title: "Customs Clearance",
    description: "Expert handling of import/export documentation and clearance processes.",
    image: "/src/img/service-5.jpg",
  },
  {
    title: "Warehouse Solutions",
    description: "Modern warehousing and inventory management tailored to your business needs.",
    image: "/src/img/service-6.jpg",
  },
];
</script>


<style scoped>
.services-section {
  background-color: #fff;
  padding-top: 80px;
  padding-bottom: 80px;
  font-family: "Poppins", sans-serif;
  color: #333;
}

/* Section Heading */
.services-section h6 {
  color: #0d6efd;
  text-transform: uppercase;
  font-weight: 700;
  letter-spacing: 1px;
  margin-bottom: 0.5rem;
}
.services-section h2 {
  font-weight: 700;
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin-bottom: 1rem;
}
.services-section p {
  color: #666;
  line-height: 1.7;
}

/* Service Cards */
.service-item {
  background: #fff;
  border-radius: 1rem;
  overflow: hidden;
  transition: all 0.5s ease;
  position: relative;
  cursor: pointer;
  border: 1px solid rgba(0, 0, 0, 0.05);
}
.service-item:hover {
  transform: translateY(-12px);
  box-shadow: 0 20px 45px rgba(0, 0, 0, 0.15);
  border-color: #0d6efd;
}

/* Card Header (Image) */
.image-wrapper {
  position: relative;
  overflow: hidden;
  border-bottom: 1px solid rgba(0, 0, 0, 0.05);
}
.image-wrapper img {
  width: 100%;
  transition: transform 0.6s ease, filter 0.6s ease;
  border-radius: 1rem 1rem 0 0;
}
.image-wrapper:hover img {
  transform: scale(1.08);
  filter: brightness(0.9);
}

/* Overlay with gradient effect */
.image-overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(135deg, #0d6efd99, #f8c14699);
  opacity: 0;
  transition: opacity 0.4s ease;
  display: flex;
  justify-content: center;
  align-items: center;
  border-radius: 1rem 1rem 0 0;
}
.image-wrapper:hover .image-overlay {
  opacity: 1;
}
.image-overlay .btn {
  background: #fff;
  color: #0d6efd;
  font-weight: 600;
  border-radius: 50px;
  padding: 0.5rem 1.5rem;
  transition: all 0.4s ease;
}
.image-overlay .btn:hover {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  color: #fff !important;
  transform: translateY(-2px) scale(1.05);
  box-shadow: 0 8px 20px rgba(13, 110, 253, 0.4);
}

/* Card Content */
.service-item h4 {
  font-weight: 600;
  margin-bottom: 0.5rem;
  transition: all 0.3s ease;
}
.service-item:hover h4 {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.service-item p {
  font-size: 0.9rem;
  color: #666;
  transition: color 0.3s ease;
}
.service-item:hover p {
  color: #0d6efd;
}

/* Responsive */
@media (max-width: 991px) {
  .services-section h2 {
    font-size: 1.75rem;
  }
  .services-section p {
    width: 100% !important;
  }
}

</style>