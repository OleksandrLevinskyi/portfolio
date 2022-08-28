<template>
  <div class="d-flex flex-column align-content-center p-3">
    <iframe class="video"
            src="https://www.youtube.com/embed/6fWU0e6W8QY"
            title="YouTube project demo"
            allowfullscreen
    ></iframe>

    <h1>Project Title
      <a href="https://github.com/OleksandrLevinskyi"
         class="ms-3"
         target=”_blank”>
        <b-icon-github class="fs-1 text-black"/>
      </a>
      <a href="https://www.youtube.com"
         class="ms-3"
         target=”_blank”>
        <b-icon-youtube class="fs-1 text-danger"/>
      </a>
    </h1>

    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi dicta, maiores necessitatibus quam quos
      recusandae saepe sequi temporibus veniam vero.</p>

    <div class="d-flex">
      <span class="badge bg-secondary me-3 fs-5">Tech</span>
      <span class="badge bg-secondary me-3 fs-5">Tech</span>
      <span class="badge bg-secondary me-3 fs-5">Tech</span>
    </div>
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
  width: 100%;
}
</style>
