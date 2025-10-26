<template>
  <section class="testimonial-section">
    <div class="container text-center">
      <h6 class="section-subtitle">TESTIMONIAL</h6>
      <h2 class="section-title">Our Clients Say!</h2>

      <div class="testimonial-grid">
        <div class="testimonial-card" v-for="(client, index) in clients" :key="index">
          <div class="quote-icon">“</div>
          <div class="client-info">
            <img :src="client.image" alt="Client" class="client-img" />
            <div>
              <h5 class="client-name">{{ client.name }}</h5>
              <p class="client-role">{{ client.profession }}</p>
            </div>
          </div>
          <p class="client-text">{{ client.text }}</p>
        </div>
      </div>

      <!-- Dots -->
      <div class="dots">
        <span v-for="(dot, i) in 3" :key="i" :class="{ active: i === 1 }"></span>
      </div>
    </div>
  </section>
</template>

<script setup>
const clients = [
  {
    name: "Client Name",
    profession: "Profession",
    image: "/src/img/testimonial-1.jpg",
    text: "Tempor erat elitr rebum at clita. Diam dolor diam ipsum sit diam amet diam et eos.",
  },
  {
    name: "Client Name",
    profession: "Profession",
    image: "/src/img/testimonial-2.jpg",
    text: "Diam dolor diam ipsum sit diam amet diam et eos. Clita erat ipsum et lorem et sit.",
  },
  {
    name: "Client Name",
    profession: "Profession",
    image: "/src/img/testimonial-3.jpg",
    text: "Clita erat ipsum et lorem et sit. Tempor erat elitr rebum at clita diam dolor diam.",
  },
];
</script>

<style scoped>
/* --- Section Styling --- */
.testimonial-section {
  background: linear-gradient(to bottom, #ffffff, #f8f9fb);
  padding: 100px 0;
  text-align: center;
}

.section-subtitle {
  background: linear-gradient(90deg, #1b3b80, #d6a354);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  text-transform: uppercase;
  font-weight: 700;
  letter-spacing: 2px;
  font-size: 0.9rem;
}

.section-title {
  font-size: 2.5rem;
  font-weight: 800;
  color: #0a0a0a;
  margin-bottom: 3rem;
}

/* --- Grid Layout --- */
.testimonial-grid {
  display: flex;
  justify-content: center;
  gap: 2.5rem;
  flex-wrap: wrap;
}

/* --- Card Design --- */
.testimonial-card {
  position: relative;
  background: #fff;
  border-radius: 18px;
  padding: 2.5rem;
  width: 330px;
  text-align: left;
  box-shadow: 0 8px 25px rgba(0, 0, 0, 0.05);
  transition: all 0.4s ease;
  border-top: 3px solid transparent;
}

.testimonial-card:hover {
  transform: translateY(-12px);
  background: linear-gradient(180deg, #ffffff, #fefcf8);
  box-shadow: 0 10px 40px rgba(27, 59, 128, 0.25);
  border-image: linear-gradient(90deg, #1b3b80, #d6a354) 1;
}

/* --- Quote Icon --- */
.quote-icon {
  position: absolute;
  top: 10px;
  right: 20px;
  font-size: 5rem;
  font-weight: 700;
  background: linear-gradient(90deg, #1b3b80, #d6a354);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  opacity: 0.08;
}

/* --- Client Info --- */
.client-info {
  display: flex;
  align-items: center;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.client-img {
  width: 70px;
  height: 70px;
  border-radius: 50%;
  object-fit: cover;
  border: 3px solid transparent;
  background: linear-gradient(90deg, #1b3b80, #d6a354);
  background-origin: border-box;
  box-shadow: 0 0 0 2px #fff;
}

.client-name {
  font-weight: 700;
  font-size: 1.05rem;
  color: #0a0a0a;
}

.client-role {
  font-size: 0.9rem;
  color: #555;
}

/* --- Testimonial Text --- */
.client-text {
  color: #444;
  font-size: 0.98rem;
  line-height: 1.8;
  font-style: italic;
}

/* --- Dots --- */
.dots {
  margin-top: 2.5rem;
}

.dots span {
  display: inline-block;
  width: 10px;
  height: 10px;
  margin: 0 5px;
  background: #d1d1d1;
  border-radius: 50%;
  transition: all 0.3s ease;
}

.dots span.active {
  background: linear-gradient(90deg, #1b3b80, #d6a354);
  transform: scale(1.3);
}
</style>
