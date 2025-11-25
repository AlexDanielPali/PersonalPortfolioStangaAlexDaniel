<script>
export default {
  name: "ExperienceSection",
  data() {
    return {
      frontendSkills: [
        { name: "HTML", level: "Experienced" },
        { name: "CSS", level: "Experienced" },
        { name: "JavaScript", level: "Intermediate" },
        { name: "Vue.js", level: "Intermediate" },
        { name: "Material UI", level: "Intermediate" },
      ],
      backendSkills: [
        { name: "PostgreSQL", level: "Basic" },
        { name: "Node JS", level: "Intermediate" },
        { name: "Git", level: "Intermediate" },
      ],
    };
  },
  methods: {
    goToProjects() {
      location.href = "#projects";
    },
  },
};
</script>

<template>
  <section id="experience" class="experience">
    <p class="section__text__p1">Explore My</p>
    <h1 class="title">Experience</h1>

    <div class="experience-details-container">
      <div class="about-containers">
        <!-- Frontend -->
        <div class="details-container">
          <h2 class="experience-sub-title">Frontend Development</h2>
          <div class="article-container">
            <article v-for="(skill, index) in frontendSkills" :key="index">
              <img src="/assets/checkmark.png" alt="Experience icon" class="icon" />
              <div>
                <h3>{{ skill.name }}</h3>
                <p>{{ skill.level }}</p>
              </div>
            </article>
          </div>
        </div>

        <!-- Backend -->
        <div class="details-container">
          <h2 class="experience-sub-title">Backend Development</h2>
          <div class="article-container">
            <article v-for="(skill, index) in backendSkills" :key="index">
              <img src="/assets/checkmark.png" alt="Experience icon" class="icon" />
              <div>
                <h3>{{ skill.name }}</h3>
                <p>{{ skill.level }}</p>
              </div>
            </article>
          </div>
        </div>
      </div>
    </div>

    <!-- Arrow -->
    <img
      src="/assets/arrow.png"
      alt="Arrow icon"
      class="icon arrow"
      @click="goToProjects"
    />
  </section>
</template>

