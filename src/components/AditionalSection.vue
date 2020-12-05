<template>
  <div class="container-fluid text-center mt-3">
      <h1 class="font-italic">Tu pokemón aleatorio</h1>
    <div class="d-flex justify-content-center flex-wrap mb-5">
      <div
        class="col-sm-6 col-xs-12 col-lg-4 mt-5"
        v-for="(poke, index) of pokes"
        :key="index"
      >
        <div class="card bg-secondary text-white">
          <div class="d-flex justify-content-center p-2">
            <!-- <img v-bind:src="poke.sprites.other.official-artwork.front_default" v-bind:alt="poke.name"> -->
            <img
              v-bind:src="poke.sprites.other['official-artwork'].front_default"
              v-bind:alt="poke.name"
            />
          </div>
          <div class="card-body text-center">
            <h2 >{{ poke.id }}</h2>
            <h5 class="card-title font-weight-bold font-italic">{{ poke.name.toUpperCase() }}</h5>
            <div class="d-flex flex-wrap justify-content-center">
              <p class="card-text mr-2 font-italic" v-for="(tipo, iid) of poke.types" :key="iid">
                {{ tipo.type.name }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

function definirID() {
  return Math.round(Math.random() * (850 - 1) + 1);
}


export default {
  name: "AditionalSection",
  data() {
    return {
      pokes: [],
    };
  },
  mounted() {
    for (let i = 0; i < 3; i++) {
      let id = definirID();
      console.log(id);
      axios.get(`https://pokeapi.co/api/v2/pokemon/${id}`).then((response) => {
        this.pokes.push(response.data);
        console.log(this.pokes);
      });
    }
  },
};
</script>

<style scoped>
</style>