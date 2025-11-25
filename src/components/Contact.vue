<script>
export default {
  name: "ContactSection",
  data() {
    return {
      email: "green_eyes_alex@yahoo.com",
      linkedinUrl:
        "https://www.linkedin.com/in/alex-daniel-st%C3%A2ng%C4%83-8b3101373/",
    };
  },
};
</script>

<template>
  <section id="contact" class="contact">
    <p class="section__text__p1">Get in Touch</p>
    <h1 class="title">Contact Me</h1>

    <div class="contact-info-upper-container">
      <!-- Email -->
      <div class="contact-info-container">
        <img
          src="/assets/email.png"
          alt="Email icon"
          class="icon contact-icon email-icon"
        />
        <p>
          <a :href="`mailto:${email}`">{{ email }}</a>
        </p>
      </div>

      <!-- LinkedIn -->
      <div class="contact-info-container">
        <img
          src="/assets/linkedin.png"
          alt="LinkedIn icon"
          class="icon contact-icon"
        />
        <p>
          <a :href="linkedinUrl" target="_blank" rel="noopener noreferrer">
            LinkedIn
          </a>
        </p>
      </div>
    </div>
  </section>
</template>

