<template>
  <div id="app">
    <div>
      <head-banner></head-banner>
    </div>

    <div>
      <div class="container-fluid">
        <section-api></section-api>
      </div>
    </div>

    <div>
      <aditional-section></aditional-section>
    </div>

    <div class="container mt-5">
      <h1 class="text-center">Equipo</h1>
      <div class="row row-cols-1 row-cols-md-3">
        <div v-for="(item, index) of team" :key="index">
          <team-card v-bind:member="item"></team-card>
        </div>
      </div>
    </div>

    <div>
      <footer-page></footer-page>
    </div>
  </div>
</template>

<script>
import HeadBanner from "./components/HeadBanner.vue";
import SectionApi from "./components/SectionApi.vue";
import AditionalSection from "./components/AditionalSection.vue";
import TeamCard from "./components/TeamCard.vue";
import FooterPage from "./components/FooterPage.vue";

export default {
  name: "App",
  components: {
    HeadBanner,
    SectionApi,
    AditionalSection,
    TeamCard,
    FooterPage,
  },
  data() {
    return {
      team: [
        {
          codigo: 1,
          nombre: "JorgeJorge Andres Galeano Bayona",
          edad: "25",
          descripcion: "Estudiante del curso Misiontic, futuro emprendedor en negocio de base digital.",
          imagen: "./imagenes/Jorge.PNG",
          profesion: "Ingeniero Mecatrónico",
        },
        {
          codigo: 2,
          nombre: "Andrés David Gómez Arroyave",
          edad: "18",
          descripcion: "Futuro ingeniero mecánico con énfasis en optimización.",
          imagen: "./imagenes/AndresGomez.PNG",
          profesion: "Estudiante",
        },
        {
          codigo: 3,
          nombre: "Alex Santiago Angel Zambrano",
          edad: "18",
          descripcion: "Futuro desarrollador y socio de empresas afines a la informática.",
          imagen: "./imagenes/AlexAngel.PNG",
          profesion: "Estudiante de programación",
        },
        {
          codigo: 4,
          nombre: "Daniel Vargas Bermudez",
          edad: "27",
          descripcion: "Estudiante del curso Misiontic, futuro emprendedor en negocio de base digital.",
          imagen: "./imagenes/DavidV.PNG",
          profesion: "Ingeniero de Alimentos",
        },
        {
          codigo: 4,
          nombre: "Edwin Basilio Felix Montaño",
          edad: "37",
          descripcion: "Especialista en redes y telecomunicaciones con experiencia en radio frecuencia y soporte técnico. Manejo de equipos de medición, análisis y pos proceso. Amplia experiencia en manejo de herramientas Ofimáticas en bases de datos y telecomunicaciones. Supervisión, gestión y coordinación de recursos como planificación, desarrollo, pruebas y mantenimiento de sistemas, capacitación, compra y/o contratación de productos y servicios.",
          imagen: "./imagenes/Edwin.PNG",
          profesion: "Ingeniero de sistemas",
        },
      ],
    };
  },
};
</script>

