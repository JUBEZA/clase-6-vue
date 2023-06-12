<template>
  <div id="app-component">
    <EjemploWatch />
    <MiComponente />
    <MiComponente firstName="Félix" />
  </div>
</template>

<script>
import EjemploWatch from './components/EjemploWatch.vue';
import MiComponente from './components/MiComponente.vue';

export default {
  name: 'App',
  components: {
    EjemploWatch,
    MiComponente,
  },
};
</script>

<style>
#app-component {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
