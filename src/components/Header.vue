<template>
  <div>
    <b-nav>
      <b-nav-item disabled>Movies Rated: {{ numMovies }}</b-nav-item>
    </b-nav>
  </div>
</template>

<script>
export default {
name: "Header",
  props: {
    movies: Array
  },
  data() {
    return {
      numMovies: this.movies.length
    }
  }
}
</script>

<style scoped>

</style>