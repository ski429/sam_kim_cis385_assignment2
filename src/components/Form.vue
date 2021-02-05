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
          <b-form-input id="input-movie-title"></b-form-input>
        </b-form-group>


        <b-form-group
          id="movie-rating"
          label-cols-sm="4"
          label-cols-lg="3"
          content-cols-sm
          content-cols-lg="7"
        >
          <b-form-rating id="movie-rating" v-model="value" no-border></b-form-rating>
        </b-form-group>
      </b-form-group>
    </b-card>



  </div>
</template>

<script>
export default {
  name: "Form",
  data() {
    return {
      value: null
    }
  }
}
</script>

<style scoped>

</style>