<template>
  <div class="text-center vh-75 d-flex flex-column justify-content-center">
    <h1 class="fw-bold">Oleksandr Levinskyi</h1>
    <p class="fs-5 m-0 fw-light">Software Developer at Vehikl</p>
    <p class="fs-5 m-0 fw-light">
      <a href="https://developers.google.com/community/gdsc"
         class="text-dark text-decoration-none"
         target=”_blank”>
        GDSC<b-icon-link45deg class="h6"/>
      </a> Mentor
    </p>
    <p class="fs-5 mb-3 fw-light">
      <a href="https://developers.google.com/community/gdg"
         class="text-dark text-decoration-none"
         target=”_blank”>
        GDG<b-icon-link45deg class="h6"/>
      </a> Lead Organizer
    </p>

    <div>
      <a href="https://github.com/OleksandrLevinskyi" target=”_blank”>
        <b-icon-github class="big-icon m-2 text-black"/>
      </a>
      <a href="https://www.linkedin.com/in/oleksandrlevinskyi" target=”_blank”>
        <b-icon-linkedin class="big-icon m-2"/>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: "About"
}
</script>

<style scoped>
.vh-75 {
  height: 75vh;
}
</style>
