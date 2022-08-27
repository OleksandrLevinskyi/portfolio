<template>
  <div class="d-flex flex-column align-content-center">
    <iframe class="video"
            src="https://www.youtube.com/embed/6fWU0e6W8QY"
            title="YouTube project demo"
            allowfullscreen
    ></iframe>

    <div class="d-flex">
      <span class="h1">Project Title</span>
      <a href="https://github.com/OleksandrLevinskyi" target=”_blank”>
        <b-icon-github class="big-icon text-black"/>
      </a>
      <a href="https://www.youtube.com" target=”_blank”>
        <b-icon-youtube class="big-icon text-danger"/>
      </a>
    </div>

    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi dicta, maiores necessitatibus quam quos
      recusandae saepe sequi temporibus veniam vero.</p>

    <span class="badge bg-secondary fs-5">Tech</span>
    <span class="badge bg-secondary fs-5">Tech</span>
    <span class="badge bg-secondary fs-5">Tech</span>
  </div>
</template>

<script>
export default {
  name: "Projects",
}
</script>

<style scoped>
.video {
  aspect-ratio: 16/9;
  width: 90%;
  margin: auto;
}
</style>
