<template>
  <div class="d-flex flex-column flex-md-row p-3 p-sm-5 mx-lg-5">
    <iframe class="video"
            :src=this.demoLink
            allowfullscreen
    ></iframe>

    <div class="description d-flex align-items-center ps-md-5">
      <div>
        <h2>
          {{ this.title }}
        </h2>
        <a :href=this.githubLink
           target=”_blank”>
          <b-icon-github class="fs-3 text-black"/>
        </a>
        <a :href=this.youtubeLink
           class="ms-3"
           target=”_blank”>
          <b-icon-youtube class="fs-3 text-danger"/>
        </a>

        <p>{{ this.description }}</p>

        <div class="d-flex flex-wrap">
          <span v-for="tech in this.technologies" :key="tech" class="badge bg-secondary me-2 mb-2">{{tech}}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "ProjectDescription",
  props: {
    title: {type: String, required: true},
    description: {type: String, required: true},
    demoLink: {type: String, required: true},
    githubLink: {type: String, required: true},
    youtubeLink: {type: String, required: true},
    technologies: {type: Array, required: true},
  },
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