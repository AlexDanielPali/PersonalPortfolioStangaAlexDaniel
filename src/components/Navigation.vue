<script>
export default {
  name: "Navbar",
  data() {
    return {
      isOpen: false
    };
  },
  methods: {
    toggleMenu() {
      this.isOpen = !this.isOpen;
    }
  }
};
</script>

<template>
  <nav class="navbar">
    <!-- Desktop Navigation -->
    <div id="desktop-nav" class="desktop-nav">
      <div class="logo">Stanga Alex-Daniel</div>
      <ul class="nav-links">
        <li><a href="#about">About</a></li>
        <li><a href="#experience">Experience</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
    </div>

    <!-- Mobile Navigation -->
    <div id="hamburger-nav" class="hamburger-nav">
      <div class="logo">Stanga Alex-Daniel</div>
      <div class="hamburger-menu">
        <div 
          class="hamburger-icon" 
          :class="{ open: isOpen }" 
          @click="toggleMenu"
        >
          <span></span>
          <span></span>
          <span></span>
        </div>
        <ul class="menu-links" :class="{ open: isOpen }">
          <li><a href="#about" @click="toggleMenu">About</a></li>
          <li><a href="#experience" @click="toggleMenu">Experience</a></li>
          <li><a href="#projects" @click="toggleMenu">Projects</a></li>
          <li><a href="#contact" @click="toggleMenu">Contact</a></li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>

</style>
