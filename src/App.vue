<template>
  <div id="app">
    <h1>Oleksandr Levinskyi</h1>
    <div id="particles-js"></div>
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

#particles-js {
  position: absolute;
  width: 100%;
  height: 100%;
  background-color: #fff;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 50% 50%;
}
</style>
