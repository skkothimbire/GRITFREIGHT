<template>
    <!-- Contact Start -->
    <div class="container-fluid overflow-hidden py-5 px-lg-0">
        <div class="container contact-page py-5 px-lg-0">
            <div class="row g-5 mx-lg-0">
                <div class="col-md-6 contact-form wow fadeIn" data-wow-delay="0.1s">
                    <h6 class="text-secondary text-uppercase">Get In Touch</h6>
                    <h1 class="mb-4">Contact For Any Query</h1>
                    <p class="mb-4">The contact form is currently inactive. Get a functional and working contact form with Ajax & PHP in a few minutes. Just copy and paste the files, add a little code and you're done. <a href="https://htmlcodex.com/contact-form">Download Now</a>.</p>
                    <div class="bg-light p-4">
                        <form>
                            <div class="row g-3">
                                <div class="col-md-6">
                                    <div class="form-floating">
                                        <input type="text" class="form-control" id="name" placeholder="Your Name">
                                        <label for="name">Your Name</label>
                                    </div>
                                </div>
                                <div class="col-md-6">
                                    <div class="form-floating">
                                        <input type="email" class="form-control" id="email" placeholder="Your Email">
                                        <label for="email">Your Email</label>
                                    </div>
                                </div>
                                <div class="col-12">
                                    <div class="form-floating">
                                        <input type="text" class="form-control" id="subject" placeholder="Subject">
                                        <label for="subject">Subject</label>
                                    </div>
                                </div>
                                <div class="col-12">
                                    <div class="form-floating">
                                        <textarea class="form-control" placeholder="Leave a message here" id="message" style="height: 100px"></textarea>
                                        <label for="message">Message</label>
                                    </div>
                                </div>
                                <div class="col-12">
                                    <button class="btn btn-primary w-100 py-3" type="submit">Send Message</button>
                                </div>
                            </div>
                        </form>
                    </div>
                </div>
                <div class="col-md-6 pe-lg-0 wow fadeInRight" data-wow-delay="0.1s">
                    <div class="position-relative h-100">
                        <iframe class="position-absolute w-100 h-100" style="object-fit: cover;"
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3001156.4288297426!2d-78.01371936852176!3d42.72876761954724!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4ccc4bf0f123a5a9%3A0xddcfc6c1de189567!2sNew%20York%2C%20USA!5e0!3m2!1sen!2sbd!4v1603794290143!5m2!1sen!2sbd"
                        frameborder="0" aria-hidden="false"
                        tabindex="0"></iframe>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <!-- Contact End -->
</template>
<style scoped> 
.contact-page h6 {
    font-weight: 700;
    letter-spacing: 1px;
    color: #0d6efd; /* primary blue */
    text-transform: uppercase;
    margin-bottom: 0.5rem;
}

.contact-page h1 {
    font-weight: 700;
    background: linear-gradient(135deg, #0d6efd, #f8c146);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin-bottom: 1rem;
}

/* Paragraphs */
.contact-page p {
    color: #666;
    line-height: 1.7;
}

/* Form styling */
.contact-page .form-control {
    border: 1px solid #ccc;
    transition: all 0.4s ease;
}

.contact-page .form-control:focus {
    border-color: #0d6efd;
    box-shadow: 0 0 6px rgba(13, 110, 253, 0.4);
}

/* Floating labels */
.contact-page .form-floating label {
    color: #666;
    transition: all 0.3s ease;
}

.contact-page .form-floating input:focus + label,
.contact-page .form-floating textarea:focus + label {
    color: #0d6efd;
}

/* Button styling */
.contact-page .btn-primary {
    background: linear-gradient(135deg, #0d6efd, #f8c146);
    border: none;
    font-weight: 600;
    transition: all 0.4s ease;
}
.contact-page .btn-primary:hover {
    transform: translateY(-2px) scale(1.02);
    box-shadow: 0 6px 15px rgba(13, 110, 253, 0.4);
}

/* Map styling */
.contact-page iframe {
    border: 0;
    border-radius: 8px;
    filter: brightness(0.95);
    transition: all 0.4s ease;
}
.contact-page iframe:hover {
    filter: brightness(1);
}

/* Background for the form container */
.contact-page .bg-light {
    background: linear-gradient(135deg, #0d6efd05, #f8c14610);
    border-radius: 8px;
    padding: 2rem;
    box-shadow: 0 10px 30px rgba(0, 0, 0, 0.05);
}

/* Responsive */
@media (max-width: 991px) {
    .contact-page .contact-form,
    .contact-page iframe {
        margin-bottom: 2rem;
    }
}

@media (max-width: 576px) {
    .contact-page h1 {
        font-size: 1.8rem;
    }
    .contact-page .btn-primary {
        padding: 0.8rem 0;
    }
}

</style>