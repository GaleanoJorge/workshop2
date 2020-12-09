<template>
  <div>
    <div class="col mb-4">
      <div class="card text-white bg-secondary mb-3">
        <img
          v-bind:src="member.imagen"
          class="card-img-top"
          alt="fotografía del equipo"
        />
        <div class="card-body">
          <h5 class="card-title">{{ member.codigo }} {{ member.nombre }}</h5>
          <p class="card-text">
              Rol: {{member.rol}} <br><br>
            {{ member.descripcion }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "TeamCard",
  props: ["member"],
};
</script>

<style scoped>
</style>
