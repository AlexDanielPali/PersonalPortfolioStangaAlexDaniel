<template>
  <section id="profile" class="profile">
    <!-- Profile Picture -->
    <div class="section__pic-container">
      <img src="/assets/profile-pic.png" alt="Alex profile picture" />
    </div>

    <!-- Profile Text -->
    <div class="section__text">
      <p class="section__text__p1">Hello, I'm</p>
      <h1 class="title">Stanga Alex-Daniel</h1>
      <p class="section__text__p2">Frontend Developer</p>

      <!-- Buttons -->
      <div class="btn-container">
        <button class="btn btn-color-2" @click="downloadCV">
          Download CV
        </button>
        <button class="btn btn-color-1" @click="goToContact">
          Contact Info
        </button>
      </div>

      <!-- Socials -->
      <div id="socials-container">
        <img
          src="/assets/linkedin.png"
          alt="My LinkedIn profile"
          class="icon"
          @click="openLink(linkedinUrl)"
        />
        <img
          src="/assets/github.png"
          alt="My Github profile"
          class="icon"
          @click="openLink(githubUrl)"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "ProfileSection",
  data() {
    return {
      cvPath: "/assets/stanga_alex_daniel_cv.pdf",
      linkedinUrl:
        "https://www.linkedin.com/in/alex-daniel-st%C3%A2ng%C4%83-8b3101373/",
      githubUrl: "https://github.com/AlexDanielPali",
    };
  },
  methods: {
    downloadCV() {
      window.open(this.cvPath, "_blank");
    },
    goToContact() {
      location.href = "#contact";
    },
    openLink(url) {
      window.open(url, "_blank");
    },
  },
};
</script>

<style scoped>

</style>
