<script>
export default {
  name: "ProjectsSection",
  data() {
    return {
      projects: [
        {
          title: "Project One",
          image: "/assets/project-1.png",
          github: "https://github.com/AlexDanielPali/TapiterieBratcaBorod",
          demo: "https://alexdanielpali.github.io/TapiterieBratcaBorod/",
        },
        {
          title: "Project Two",
          image: "/assets/project-2.png",
          github: "https://github.com/AlexDanielPali/pavaje-bratca-website",
          demo: "https://alexdanielpali.github.io/pavaje-bratca-website/",
        },
        {
          title: "Project Three",
          image: "/assets/project-3.png",
          github:
            "https://github.com/AlexDanielPali/HexSoftwares_ToDoList_Stanga_Alex_Daniel/",
          demo: "https://alexdanielpali.github.io/HexSoftwares_ToDoList_Stanga_Alex_Daniel/",
        },
        {
          title: "Project Four",
          image: "/assets/project-4.png",
          github:
            "https://github.com/AlexDanielPali/HexSoftwares_AnimalCharityWebsite_Stanga_Alex_Daniel",
          demo: "https://alexdanielpali.github.io/HexSoftwares_AnimalCharityWebsite_Stanga_Alex_Daniel/",
        },
        {
          title: "Project Five",
          image: "/assets/project-5.png",
          github:
            "https://github.com/AlexDanielPali/HexSoftwares_MusicPlayer_Stanga_Alex_Daniel/",
          demo: "https://papaya-valkyrie-ff8852.netlify.app/",
        },
        {
          title: "Project Six",
          image: "/assets/project-6.png",
          github:
            "https://github.com/AlexDanielPali/HexSoftwares_AnimatedWebsite_Stanga_Alex_Daniel",
          demo: "https://alexdanielpali.github.io/HexSoftwares_AnimatedWebsite_Stanga_Alex_Daniel/",
        },
      ],
    };
  },
  methods: {
    openLink(url) {
      window.open(url, "_blank");
    },
    goToContact() {
      location.href = "#contact";
    },
  },
};
</script>

<template>
  <section id="projects" class="projects">
    <p class="section__text__p1">Browse My</p>
    <h1 class="title">Frontend Projects</h1>

    <div class="experience-details-container">
      <div class="about-containers">
        <!-- Loop through projects -->
        <div
          v-for="(project, index) in projects"
          :key="index"
          class="details-container color-container"
        >
          <div class="article-container">
            <img :src="project.image" :alt="project.title" class="project-img" />
          </div>
          <h2 class="experience-sub-title project-title">{{ project.title }}</h2>
          <div class="btn-container">
            <button
              class="btn btn-color-2 project-btn"
              @click="openLink(project.github)"
            >
              Github
            </button>
            <button
              class="btn btn-color-2 project-btn"
              @click="openLink(project.demo)"
            >
              Live Demo
            </button>
          </div>
        </div>
      </div>
    </div>

    <!-- Arrow -->
    <img
      src="/assets/arrow.png"
      alt="Arrow icon"
      class="icon arrow"
      @click="goToContact"
    />
  </section>
</template>

