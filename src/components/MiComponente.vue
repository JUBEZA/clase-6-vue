<template>
  <p class="card">Hola {{ prefijo }} {{ firstName }}</p>
  <button @click="nuevoAlumno">Añadir a Esteban</button>
  <ul>
    <li v-for="(alumno, i) in alumnos" :key="i">
      <UnAlumno :name="alumno">
    </li>
  </ul>
</template>

<script>
import UnAlumno from './UnAlumno.vue';

export default {
  name: 'MiComponente',
  components: {
    UnAlumno
  },
  props: {
    firstName: {
      type: String,
      default: 'Santiago',
    },
    lastName: String,
  },
  data() {
    return {
      prefijo: 'Mr.',
      alumnos: ['Santiago', 'Andrés', 'Fidel', 'Carolina'],
    };
  },
  methods: {
    nuevoAlumno() {
      this.alumnos.push("Esteban")
    }
  }
};
</script>

<style scoped>
.card {
  background: blue;
  color: white;
}
</style>
