<template>
  <div>
    <b-embed
        class="w-50 video"
        type="iframe"
        src="https://www.youtube.com/embed/6fWU0e6W8QY"
        allowfullscreen
    ></b-embed>
    <h1>Project Title</h1>
    <b-link href="https://github.com/OleksandrLevinskyi" target=”_blank”>
      <b-icon-github class="text-black"/>
    </b-link>
    <b-link href="https://www.youtube.com" target=”_blank”>
      <b-icon-youtube class="text-danger"/>
    </b-link>
    <b-badge class="bg-dark fs-5">Tech</b-badge>
    <b-badge class="bg-dark fs-5">Tech</b-badge>
    <b-badge class="bg-dark fs-5">Tech</b-badge>
    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi dicta, maiores necessitatibus quam quos
      recusandae saepe sequi temporibus veniam vero.</p>
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
}
</style>
