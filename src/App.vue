<template>
  <div id="app">
    <show-student></show-student>
  </div>
</template>

<script>
import ShowStudent from './components/student/ShowStudent.vue'

export default {
  name: 'app',
  components: {
    ShowStudent
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
