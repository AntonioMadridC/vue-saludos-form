<template>
  <div id="app">
    <saludos-form></saludos-form>
    <br class="m-5">
    <edad-form></edad-form>
  </div>
</template>

<script>
import EdadForm from './components/EdadForm.vue'
import SaludosForm from './components/SaludosForm.vue'


export default {
  name: 'App',
  components: {
    SaludosForm,
    EdadForm
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
