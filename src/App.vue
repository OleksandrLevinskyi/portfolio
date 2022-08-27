<template>
  <div>
    <div id="particles-js"></div>
    <b-container class="w-100 p-0">
      <b-row align-h="around" class="w-100 text-center mx-auto nav-nowrap py-2">
        <b-col class="nav-option">
          <b-link id="about" href="#/about" class="text-decoration-none text-black fs-4 fw-light">About</b-link>
        </b-col>
        <b-col class="nav-option">
          <b-link id="projects" href="#/projects" class="text-decoration-none text-black fs-4 fw-light">Projects
          </b-link>
        </b-col>
        <b-col class="nav-option">
          <b-link id="community" href="#/community" class="text-decoration-none text-black fs-4 fw-light">Community
          </b-link>
        </b-col>
      </b-row>
    </b-container>
    <component :is="displayedComponent"/>
  </div>
</template>

<script>
import "particles.js";
import {particlesConfig} from "./particles-config";
import About from "./components/About";
import Projects from "./components/Projects";
import Community from "./components/Community";

const routes = {
  '/about': About,
  '/projects': Projects,
  '/community': Community,
}

export default {
  name: 'App',
  components: {},
  data() {
    return {currentPath: window.location.hash};
  },
  computed: {
    displayedComponent() {
      return routes[this.currentPath.slice(1) || '/'] || About
    }
  },
  methods: {
    updateNavBarStyling() {
      ["about", "projects", "community"].forEach(id => document.getElementById(id)?.classList.remove("text-decoration-underline"));
      const currentlySelectedLink = document.getElementById(this.currentPath.slice(2) || "about");
      currentlySelectedLink?.classList.add("text-decoration-underline");
    },
  },
  mounted() {
    window.particlesJS("particles-js", particlesConfig);

    this.updateNavBarStyling();

    window.addEventListener('hashchange', () => {
      this.currentPath = window.location.hash;
      this.updateNavBarStyling();
    });
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300&display=swap');

body {
  margin: 0;
  font-family: 'Space Grotesk', sans-serif;
}

.nav-nowrap {
  white-space: nowrap;
  overflow-x: auto;
}

.nav-option {
  display: inline-block;
  float: none;
}

canvas {
  display: block;
  vertical-align: bottom;
}

#particles-js {
  z-index: -1;
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: #fff;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
}
</style>
