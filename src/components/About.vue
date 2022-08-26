<template>
  <b-row class="text-center pt-5 m-0 vh-75" align-v="center">
    <b-col>
      <h1 class="fw-bold">Oleksandr Levinskyi</h1>
      <p class="fs-5 pb-3 fw-light">Software Developer at Vehikl -
        <b-link href="https://developers.google.com/community/gdsc" class="text-dark text-decoration-none" target=”_blank”>GDSC<b-icon-link45deg class="h6"/>
        </b-link>
        Mentor -
        <b-link href="https://developers.google.com/community/gdg" class="text-dark text-decoration-none"
                target=”_blank”>GDG<b-icon-link45deg class="h6"/>
        </b-link>
        Lead
        Organizer
      </p>

      <div>
        <b-link href="https://github.com/OleksandrLevinskyi" target=”_blank”>
          <b-icon-github class="big-icon m-2 text-black"/>
        </b-link>
        <b-link href="https://www.linkedin.com/in/oleksandrlevinskyi" target=”_blank”>
          <b-icon-linkedin class="big-icon m-2"/>
        </b-link>
      </div>
    </b-col>
  </b-row>
</template>

<script>
export default {
  name: "About"
}
</script>

<style scoped>
.big-icon {
  font-size: 2.5rem;
}

.vh-75 {
  height: 75vh;
}
</style>
