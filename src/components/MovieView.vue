<template>
  <div>
    <ul id="movie-list">
      <li v-for="movie in movies" :key="movie.title">
        {{ movie.title}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MovieView",
  data() {
    return {
      title: ""
    }
  },
  props: {
    movies: Array
  }
}
</script>

<style scoped>

</style>