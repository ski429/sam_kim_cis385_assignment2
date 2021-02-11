<template>
  <div>
    <ul id="movie-list">
      <li v-for="movie in movies" :key="movie.title">
        {{ movie.title}}<br>
        {{ movie.rating}}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "MovieView",
  data() {
    return {
      title: "",
      rating: null
    }
  },
  props: {
    movies: Array
  }
}
</script>

<style scoped>

</style>