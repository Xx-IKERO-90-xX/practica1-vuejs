<template>
    <h1>Gestion de Vehículos</h1>
    <div>
      <Coche />
    </div>
    <div>
      <Avion />
    </div>
    <div>
      <Moto />
    </div>
</template>

<script>
import Coche from "./components/Car.vue"
import Avion from "./components/Avion.vue"
import Moto from "./components/Moto.vue"

export default {
  name: 'App',
  components: {
    Coche,
    Avion,
    Moto
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: left;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
