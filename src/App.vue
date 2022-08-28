<template>
  <div>
    <div id="particles-js"></div>

    <div class="container">
      <div class="row py-2 d-flex flex-nowrap horizontal-scroll">
        <div class="col-6 col-sm-4 d-flex justify-content-center">
          <a id="about" href="#/about" class="text-decoration-none text-black fs-4 fw-light">About</a>
        </div>
        <div class="col-6 col-sm-4 d-flex justify-content-center">
          <a id="projects" href="#/projects" class="text-decoration-none text-black fs-4 fw-light">Projects</a>
        </div>
        <div class="col-6 col-sm-4 d-flex justify-content-center">
          <a id="community" href="#/community" class="text-decoration-none text-black fs-4 fw-light">Community</a>
        </div>
      </div>
      <div id="scroll-menu-label" class="row text-center display-none">
        <p>
          <b-icon-arrow-left class="text-black"/>
          scroll menu
          <b-icon-arrow-right class="text-black"/>
        </p>
      </div>
    </div>

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

.horizontal-scroll {
  white-space: nowrap;
  overflow-x: auto;
}

.big-icon {
  font-size: 2.5rem;
}

@media only screen and (min-width: 576px) {
  #scroll-menu-label {
    display: none;
  }
}

/*** background ***/
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
