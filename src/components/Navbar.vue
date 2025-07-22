<template>
  <nav :class="['navbar', { 'visible': isSticky }]">
    <ul class="nav-links">
      <li><a :class="{ active: currentSection === 'about' }" href="#about">About</a></li>
      <li><a :class="{ active: currentSection === 'timeline' }" href="#timeline">Education</a></li>
      <li><a :class="{ active: currentSection === 'skills' }" href="#skills">Skills</a></li>
      <li><a :class="{ active: currentSection === 'projects' }" href="#projects">Projects</a></li>
      <li><a :class="{ active: currentSection === 'contact' }" href="#contact">Contact</a></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "Navbar",
  props: {
    currentSection: String,
  },
  data() {
    return {
      isSticky: false,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  beforeUnmount() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      this.isSticky = window.scrollY > window.innerHeight - 10;
    },
  },
};
</script>

<style scoped>
.navbar {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  padding: 1rem 2rem;
  background: rgba(15, 32, 39, 0.74);
  backdrop-filter: blur(25px);
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.349);
  transform: translateY(-100%);
  transition: transform 0.3s ease-in-out;
  z-index: 1000;
}

.navbar.visible {
  transform: translateY(0);
}

.nav-links {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 2rem;
  list-style: none;
  margin: 0 auto;
  padding: 0;
  width: 100%;
  max-width: 1200px;
}

.nav-links li {
  list-style: none;
}

.nav-links a {
  position: relative;
  text-decoration: none;
  color: #c2e9fb;
  font-weight: bold;
  font-size: 1.1rem;
  transition: color 0.3s;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
}

.nav-links a::after {
  content: "";
  position: absolute;
  bottom: -4px;
  left: 12.5%; /* center the 75% width underline */
  width: 75%;
  height: 2px;
  background-color: #9aadff;
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.3s ease-in-out;
  border-radius: 1px;
}

/* Hover effect */
.nav-links a:hover::after {
  transform: scaleX(1);
}

/* Active state */
.nav-links a.active {
  color: #3b5fff;
}

.nav-links a.active::after {
  transform: scaleX(1);
}
</style>
