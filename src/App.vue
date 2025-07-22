<template>
  <div id="app">
    <Navbar :currentSection="activeSection" />
    <Home @updateSection="activeSection = $event" />
  </div>
</template>

<script>
import Navbar from "./components/Navbar.vue";
import Home from "./views/Home.vue";

export default {
  components: {
    Navbar,
    Home,
  },
  data() {
    return {
      activeSection: "about",
    };
  },
};
</script>

<style>
* {
  box-sizing: border-box;
}
html {
  scroll-behavior: smooth;
  font-family: 'Segoe UI', sans-serif;
}

section {
  scroll-margin-top: 7px;
}

body {
  margin: 0;
  font-family: 'Inter', sans-serif;
  background-color: #0f2027;
  color: white;
  scroll-behavior: smooth;
}


</style>
