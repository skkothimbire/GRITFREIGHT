<template>
  <!-- Team Section -->
  <section class="team-section py-5">
    <div class="container-fluid px-lg-5 px-md-4 px-3">
      <!-- Section Header -->
      <div
        class="text-center mb-5 animate__animated animate__fadeInUp"
        data-wow-delay="0.1s"
      >
        <h6 class="text-primary text-uppercase fw-bold mb-2">Our Team</h6>
        <h2 class="fw-bold display-6">Expert Team Members</h2>
      </div>

      <!-- Team Grid -->
      <div class="row g-4 justify-content-center">
        <div
          v-for="(member, index) in teamMembers"
          :key="index"
          class="col-xl-3 col-lg-4 col-md-6"
        >
          <div class="team-card position-relative overflow-hidden rounded-4">
            <div class="team-img-wrapper">
              <img
                :src="member.image"
                class="img-fluid w-100 team-img"
                :alt="member.name"
              />
            </div>

            <div class="team-info text-center p-4">
              <h5 class="fw-bold mb-1">{{ member.name }}</h5>
              <p class="text-muted mb-3">{{ member.designation }}</p>
              <div class="team-social d-flex justify-content-center gap-3">
                <a
                  v-for="(icon, i) in member.social"
                  :key="i"
                  :href="icon.link"
                  target="_blank"
                  rel="noopener"
                >
                  <i :class="icon.icon"></i>
                </a>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const teamMembers = [
  {
    name: "John Doe",
    designation: "CEO",
    image: "/src/img/team-1.jpg",
    social: [
      { icon: "fab fa-facebook-f", link: "#" },
      { icon: "fab fa-twitter", link: "#" },
      { icon: "fab fa-linkedin-in", link: "#" },
    ],
  },
  {
    name: "Jane Smith",
    designation: "Operations Manager",
    image: "/src/img/team-2.jpg",
    social: [
      { icon: "fab fa-facebook-f", link: "#" },
      { icon: "fab fa-twitter", link: "#" },
      { icon: "fab fa-linkedin-in", link: "#" },
    ],
  },
  {
    name: "Alice Johnson",
    designation: "Logistics Head",
    image: "/src/img/team-3.jpg",
    social: [
      { icon: "fab fa-facebook-f", link: "#" },
      { icon: "fab fa-twitter", link: "#" },
      { icon: "fab fa-linkedin-in", link: "#" },
    ],
  },
  {
    name: "Bob Williams",
    designation: "Freight Coordinator",
    image: "/src/img/team-4.jpg",
    social: [
      { icon: "fab fa-facebook-f", link: "#" },
      { icon: "fab fa-twitter", link: "#" },
      { icon: "fab fa-linkedin-in", link: "#" },
    ],
  },
];
</script>

<style scoped>
.team-section {
  background: #f8f9fa;
}

/* === Team Card (Exact Same as Feature/Why Choose Us) === */
.team-card {
  background: rgba(255, 255, 255, 0.7);
  backdrop-filter: blur(14px);
  border-radius: 1.25rem;
  border: 1px solid rgba(255, 215, 0, 0.35);
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.05);
  transition: all 0.45s ease;
}

.team-card:hover {
  transform: translateY(-12px);
  border-color: rgba(255, 215, 0, 0.75);
  box-shadow: 0 0 25px rgba(255, 215, 0, 0.4);
  background: linear-gradient(
    145deg,
    rgba(255, 255, 255, 0.9),
    rgba(255, 215, 0, 0.15)
  );
}

/* === Image Section === */
.team-img-wrapper {
  overflow: hidden;
  border-radius: 1.25rem 1.25rem 0 0;
}

.team-img {
  height: 280px;
  object-fit: cover;
  transition: all 0.6s ease;
}

.team-card:hover .team-img {
  transform: scale(1.07);
  filter: brightness(1.1);
}

/* === Info Text === */
.team-info h5 {
  color: #212529;
}

.team-info p {
  color: #6c757d;
}

/* === Social Icons === */
.team-social a i {
  color: #6c757d;
  font-size: 1rem;
  transition: all 0.3s ease;
}

.team-social a i:hover {
  color: #f8c146;
}

/* === Responsive === */
@media (max-width: 991.98px) {
  .team-img {
    height: 250px;
  }
}
</style>
