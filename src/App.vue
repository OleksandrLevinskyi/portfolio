<template>
  <div>
    <div id="particles-js"></div>
    <b-container class="w-100">
<!--      <b-row class="text-center mb-0">-->
<!--        <p>&lt;&lt;&lt; scroll &gt;&gt;&gt;</p>-->
<!--      </b-row>-->
      <b-row align-h="around" class="w-100 text-center mx-auto nav-nowrap py-2">
        <b-col cols="2" class="nav-option">
          <b-link href="#/about" class="text-decoration-underline text-black fs-3 fw-light">About</b-link>
        </b-col>
        <b-col cols="2" class="nav-option">
          <b-link href="#/projects" class="text-decoration-none text-black fs-3 fw-light">Projects</b-link>
        </b-col>
        <b-col cols="2" class="nav-option">
          <b-link href="#/community" class="text-decoration-none text-black fs-3 fw-light">Community</b-link>
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
  mounted() {
    window.particlesJS("particles-js", particlesConfig);

    window.addEventListener('hashchange', () => {
      this.currentPath = window.location.hash
    })
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@300&display=swap');

body {
  margin: 0;
  font-family: 'Space Grotesk', sans-serif;
}

.nav-nowrap{
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
