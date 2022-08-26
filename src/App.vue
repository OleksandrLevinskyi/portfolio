<template>
  <div>
    <div id="particles-js"></div>
    <b-navbar toggleable="sm" class="pb-5">
      <b-navbar-toggle target="nav-collapse" class="ms-4"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="w-100">
          <b-row align-h="around" class="w-100 text-center mx-auto text-black">
            <b-col cols="2">
              <b-nav-item href="#/about" class="text-decoration-underline">ABOUT</b-nav-item>
            </b-col>
            <b-col cols="2">
              <b-nav-item href="#/projects">PROJECTS</b-nav-item>
            </b-col>
            <b-col cols="2">
              <b-nav-item href="#/community">COMMUNITY</b-nav-item>
            </b-col>
          </b-row>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
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
    return {
      currentPath: window.location.hash
    }
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
