<template>
  <div>
    <b-card bg-variant="light">
      <b-form-group
        id="movie"
        label-cols-lg="3"
        label-size="lg"
        label-class="font-weight-bold"
        label="Movie"
      >
        <b-form-group
          id="movie-tile"
          label-cols-sm="4"
          label-cols-lg="3"
          content-cols-sm
          content-cols-lg="7"
          label="Title"
        >
          <b-form-input id="input-movie-title" v-model="title"></b-form-input>
        </b-form-group>


        <b-form-group
          id="movie-rating"
          label-cols-sm="4"
          label-cols-lg="3"
          content-cols-sm
          content-cols-lg="7"
        >
          <b-form-rating id="movie-rating" v-model.number="rating" no-border></b-form-rating>
        </b-form-group>
        <b-button
            :disabled="title.length < 1 || !rating"
            @click="add"
        >
          Submit
        </b-button>
      </b-form-group>
    </b-card>



  </div>
</template>

<script>
export default {
  name: "Form",
  props : {
    movies: Array
  },
  data() {
    return {
      rating: 0,
      title: ""
    }
  },
  methods : {
    add: function() {
      this.movies.push({ "title": this.title, "rating": this.rating })
      this.title = ""
      this.rating = 0
    }
  }
}
</script>

<style scoped>

</style>