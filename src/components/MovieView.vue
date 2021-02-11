<template>
  <div>
    <table class="center">
      <tr>
        <th>Movie Title</th>
        <th>Your Rating</th>
      </tr>
      <tr v-for="movie in movies" :key="movie.title">
        <td>{{ movie.title }}</td>
        <td>{{ movie.rating }}/5</td>
      </tr>
    </table>
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
  div {
    margin: 20px 20px;
  }

  .center {
    margin-left: auto;
    margin-right: auto;
  }

  th, td {
    padding: 10px;
  }
</style>