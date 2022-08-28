<template>
  <div class="d-flex flex-column flex-md-row p-3 p-sm-5 mx-lg-5">
    <iframe class="video"
            src="https://www.youtube.com/embed/6fWU0e6W8QY"
            title="YouTube project demo"
            allowfullscreen
    ></iframe>

    <div class="description d-flex align-items-center ps-md-5">
      <div>
        <h2>Project Title
          <a href="https://github.com/OleksandrLevinskyi"
             class="ms-3"
             target=”_blank”>
            <b-icon-github class="fs-3 text-black"/>
          </a>
          <a href="https://www.youtube.com"
             class="ms-3"
             target=”_blank”>
            <b-icon-youtube class="fs-3 text-danger"/>
          </a>
        </h2>

        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi dicta, maiores necessitatibus quam quos
          recusandae saepe sequi temporibus veniam vero.</p>

        <div class="d-flex">
          <span class="badge bg-secondary me-3 fs-6">Tech</span>
          <span class="badge bg-secondary me-3 fs-6">Tech</span>
          <span class="badge bg-secondary me-3 fs-6">Tech</span>
        </div>
      </div>
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

@media (min-width: 768px) {
  .video {
    width: 60%;
  }

  .description {
    width: 40%;
  }
}

@media (min-width: 1200px) {
  .video, .description {
    width: 50%;
  }
}
</style>
