<template>
  <div id="app">
    <Header/>
    <Form
        :movies="movies"
    />
    <MovieView :movies="movies"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Form from './components/Form.vue'
import MovieView from "@/components/MovieView";

export default {
  name: 'App',
  components: {
    Header,
    Form,
    MovieView
  },
  data() {
    return {
      movies: []
    }
  }

}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
