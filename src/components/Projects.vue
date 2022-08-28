<template>
  <div>
    <project-description title="Project Title"
                         description="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Accusamus, placeat?"
                         demo-link="https://www.youtube.com/embed/6fWU0e6W8QY" github-link="https://github.com/"
                         youtube-link="https://www.youtube.com/"
                         :technologies="['Tech 1','Tech 2','Tech 3','Tech 4','Tech 5']"/>
  </div>
</template>

<script>
import ProjectDescription from "./ProjectDescription";

export default {
  name: "Projects",
  components: {ProjectDescription},
}
</script>

<style scoped>
</style>
