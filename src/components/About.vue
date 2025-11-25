<script>
export default {
  name: "AboutSection",
  methods: {
    goToExperience() {
      location.href = "#experience";
    },
  },
};
</script>

<template>
  <section id="about" class="about">
    <p class="section__text__p1">Get To Know More</p>
    <h1 class="title">About Me</h1>

    <div class="section-container">
      <!-- Profile Picture -->
      <div class="section__pic-container">
        <img
          src="/assets/about-pic.png"
          alt="Profile picture"
          class="about-pic"
        />
      </div>

      <!-- About Details -->
      <div class="about-details-container">
        <div class="about-containers">
          <!-- Experience -->
          <div class="details-container">
            <img
              src="/assets/experience.png"
              alt="Experience icon"
              class="icon"
            />
            <h3>Experience</h3>
            <p>1 year <br />Frontend Development</p>
          </div>

          <!-- Education -->
          <div class="details-container">
            <img
              src="/assets/education.png"
              alt="Education icon"
              class="icon"
            />
            <h3>Education</h3>
            <p>B.Sc. Bachelors Degree</p>
          </div>
        </div>

        <!-- About Text -->
        <div class="text-container">
          <p>
            Dynamic Frontend Developer passionate about building responsive, high-performance web applications using Vue.js,
            JavaScript (ES6+), HTML5, and CSS3. Experienced in translating UI/UX designs into intuitive, accessible, and scalable
            interfaces that enhance user engagement and performance. Skilled in Agile workflows, Git-based collaboration, and
            delivering clean, maintainable code that drives measurable results.
          </p>
        </div>
      </div>
    </div>

    <!-- Arrow -->
    <img
      src="/assets/arrow.png"
      alt="Arrow icon"
      class="icon arrow"
      @click="goToExperience"
    />
  </section>
</template>



<style>

</style>
