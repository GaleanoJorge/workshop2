<template>
  <div>
    <div class="row mt-md-5 mt-sm-5 mt-xs-5">
      <div
        class="col-lg-6 col-xs-12"
        v-for="(movie, index) of movies"
        :key="index"
      >
        <div class="d-flex justify-content-center align-items-center">
          <div class="p-3">
            <img :src="movie.Poster" alt="poster de la peli" />
          </div>
          <div class="p-2">
            <h5>{{ movie.Title }}</h5>
            <hr />
            <p>
              ¡Una nueva amenaza se presenta en la galaxia! Luke Skywalker, en
              compañia de sus compañeros tendra que viajar a través del espacio
              sideral para restituir la paz y el equilibrio de la fuerza en el
              universo.
              <br />
              <span>Año de lanzamiento: {{ movie.Year }}</span>
            </p>
          </div>
        </div>
        <div class="d-flex container-fluid justify-content-end pb-2 mt-n2">
          <a
            :href="'https://www.imdb.com/title/' + movie.imdbID"
            target="_blank"
            class="btn btn-outline-info"
            >Info</a
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "SectionApi",
  data() {
    return {
      movies: null,
    };
  },
  mounted() {
    axios
      .get("http://www.omdbapi.com/?s=Star+wars&type=movie&apikey=8e35a43a")
      .then((response) => {
        this.movies = response.data.Search.slice(0, 4);
        console.log(this.movies);
      });
  },
};
</script>

<style scoped>
</style>