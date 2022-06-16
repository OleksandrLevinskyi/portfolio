<template>
  <div id="app">
    <div id="particles-js"></div>
    <b-navbar toggleable="sm" class="pb-5">
      <b-navbar-toggle target="nav-collapse" class="ms-4"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav class="mx-auto">
          <b-nav-item class="px-5" href="#" active>About</b-nav-item>
          <b-nav-item class="px-5" href="#">Projects</b-nav-item>
          <b-nav-item class="px-5" href="#">Community</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    <b-row class="text-center pt-5">
      <h1>Oleksandr Levinskyi</h1>

      <div>
        <b-link href="https://github.com/OleksandrLevinskyi" target=”_blank”>
          <b-icon-github class="h1 m-2 text-black"/>
        </b-link>
        <b-link href="https://www.linkedin.com/in/oleksandrlevinskyi" target=”_blank”>
          <b-icon-linkedin class="h1 m-2"/>
        </b-link>
        <b-link href="https://www.youtube.com/channel/UCicx8-vwGbcytSferp2_iQg" target=”_blank”>
          <b-icon-youtube class="h1 m-2 text-danger"/>
        </b-link>
      </div>

      <p class="text-med pt-5">I am a Software Developer at Vehikl.</p>
      <p class="text-med">I am also a Google Developer Student Club Lead.</p>
    </b-row>
  </div>
</template>

<script>
import "particles.js";
import {particlesConfig} from "./particles-config";

export default {
  name: 'App',
  components: {},
  mounted() {
    window.particlesJS("particles-js", particlesConfig);
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

.text-med{
  font-size: 1.1rem;
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
