<template>
  <!-- Footer Start -->
  <footer class="footer text-light pt-5 mt-5">
    <div class="container py-5">
      <div class="row g-5">
        <!-- Company Info -->
        <div class="col-lg-3 col-md-6 fade-in">
          <h4 class="text-uppercase mb-4 fw-bold text-primary">Gritfreight</h4>
          <p class="small text-muted">
            Delivering trust, speed, and reliability across air, sea, and road freight.
            Your global logistics partner ensuring smooth and timely transport.
          </p>
          <div class="d-flex justify-content-lg-start justify-content-center pt-3 flex-wrap social-buttons">
            <a class="btn btn-outline-light btn-social" href="#"><i class="fab fa-twitter"></i></a>
            <a class="btn btn-outline-light btn-social" href="#"><i class="fab fa-facebook-f"></i></a>
            <a class="btn btn-outline-light btn-social" href="#"><i class="fab fa-linkedin-in"></i></a>
            <a class="btn btn-outline-light btn-social" href="#"><i class="fab fa-youtube"></i></a>
          </div>
        </div>

        <!-- Address -->
        <div class="col-lg-3 col-md-6 fade-in delay-1">
          <h4 class="text-uppercase mb-4 fw-bold text-primary">Contact</h4>
          <p><i class="fa fa-map-marker-alt me-3 text-primary"></i>123 Street, New York, USA</p>
          <p><i class="fa fa-phone-alt me-3 text-primary"></i>+012 345 67890</p>
          <p><i class="fa fa-envelope me-3 text-primary"></i>info@gritfreight.com</p>
        </div>

        <!-- Quick Links -->
        <div class="col-lg-3 col-md-6 fade-in delay-2">
          <h4 class="text-uppercase mb-4 fw-bold text-primary">Quick Links</h4>
          <ul class="footer-links">
            <li><a href="#">About Us</a></li>
            <li><a href="#">Our Services</a></li>
            <li><a href="#">Contact</a></li>
            <li><a href="#">Privacy Policy</a></li>
            <li><a href="#">Terms & Conditions</a></li>
          </ul>
        </div>

        <!-- Working Hours -->
        <div class="col-lg-3 col-md-6 fade-in delay-3">
          <h4 class="text-uppercase mb-4 fw-bold text-gold working-hours-title">Working Hours</h4>
          <div class="working-hours">
            <p><span>Mon - Fri:</span> 9:00 AM - 6:00 PM</p>
            <p><span>Saturday:</span> 9:00 AM - 2:00 PM</p>
            <p><span>Sunday:</span> Closed</p>
          </div>
        </div>
      </div>
    </div>

    <!-- Divider -->
    <div class="footer-divider"></div>

    <!-- Copyright -->
    <div class="footer-bottom text-center py-3">
      <small>
        &copy; <span class="text-primary">Gritfreight</span> 2025. All Rights Reserved |
        Designed by <a href="#" target="_blank">DeployX</a>
      </small>
    </div>
  </footer>
  <!-- Footer End -->
</template>

<style scoped>
.footer {
  position: relative;
  background: linear-gradient(135deg, #0a0a0a, #121212);
  color: #bbb;
  backdrop-filter: blur(10px);
  border-top: 2px solid rgba(255, 255, 255, 0.05);
  overflow: hidden;
  font-family: "Poppins", sans-serif;
}

/* Footer Headings Gradient */
.footer h4 {
  letter-spacing: 1px;
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  font-weight: 700;
  margin-bottom: 1rem;
}

/* Quick Links */
.footer-links {
  list-style: none;
  padding: 0;
  margin: 0;
}
.footer-links li {
  margin: 10px 0;
}
.footer-links a {
  color: #bbb;
  text-decoration: none;
  transition: all 0.4s ease;
  position: relative;
  padding-bottom: 2px;
}
.footer-links a::before {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 0%;
  height: 2px;
  background: linear-gradient(90deg, #0d6efd, #f8c146);
  border-radius: 5px;
  transition: width 0.4s ease;
}
.footer-links a:hover::before {
  width: 100%;
}
.footer-links a:hover {
  color: #fff;
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

/* Working Hours */
.working-hours p {
  margin-bottom: 6px;
  display: flex;
  justify-content: space-between;
  border-bottom: 1px dashed rgba(255, 255, 255, 0.08);
  padding-bottom: 4px;
  transition: all 0.4s ease;
}
.working-hours p span {
  color: #bbb;
  font-weight: 500;
}
.working-hours p:hover {
  background: linear-gradient(135deg, #0d6efd1a, #f8c14633);
  border-radius: 4px;
  transform: translateX(4px);
  color: #fff;
}

/* Social Buttons Gradient */
.btn-social {
  width: 42px;
  height: 42px;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 5px 8px;
  color: #fff;
  border: 1px solid rgba(255, 255, 255, 0.2);
  background: linear-gradient(135deg, #0a0a0a, #121212);
  transition: all 0.4s ease;
}
.btn-social:hover {
  background: linear-gradient(135deg, #0d6efd, #f8c146);
  border-color: #f8c146;
  transform: translateY(-4px) scale(1.1);
  box-shadow: 0 0 12px rgba(13, 110, 253, 0.5);
  color: #fff;
}

/* Fade-in animation for footer sections */
.fade-in {
  opacity: 0;
  transform: translateY(20px);
  animation: fadeInUp 0.8s ease forwards;
}
.delay-1 {
  animation-delay: 0.2s;
}
.delay-2 {
  animation-delay: 0.4s;
}
.delay-3 {
  animation-delay: 0.6s;
}
@keyframes fadeInUp {
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Divider */
.footer-divider {
  width: 90%;
  height: 1px;
  background: rgba(255, 255, 255, 0.08);
  margin: 20px auto 0;
}

/* Bottom Bar */
.footer-bottom {
  background-color: #0a0a0a;
  font-size: 0.9rem;
  color: #888;
}
.footer-bottom a {
  color: #0d6efd;
  text-decoration: none;
  transition: 0.3s;
}
.footer-bottom a:hover {
  text-decoration: underline;
  color: #f8c146;
}

/* Responsive Styles */
@media (max-width: 991px) {
  .footer {
    text-align: center;
  }
  .footer h4 {
    margin-bottom: 1rem;
  }
  .footer p {
    font-size: 0.95rem;
  }
  .footer-links a {
    font-size: 0.95rem;
  }
  .social-buttons {
    justify-content: center !important;
    margin-top: 10px;
  }
  .working-hours p {
    justify-content: center;
    gap: 10px;
  }
}

@media (max-width: 576px) {
  .footer {
    padding: 20px 10px;
  }
  .btn-social {
    width: 38px;
    height: 38px;
    margin: 6px;
  }
  .footer-links li {
    margin: 8px 0;
  }
}

</style>
