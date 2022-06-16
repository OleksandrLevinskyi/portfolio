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
    <h1 class="fit-content mx-auto pt-5">Oleksandr Levinskyi</h1>
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

.fit-content {
  width: fit-content;
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
