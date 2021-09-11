<template>
  <div>
    <img alt="Vue logo" src="./assets/bird.gif">
    <Historia msg="Bienvenido a tu cAPPmino" :Historia="datos.text"/>
    <Opciones :opciones="datos.opciones"/>
  </div>
</template>

<script>
import Historia from './components/Historia.vue'
import Opciones from './components/Opciones.vue'

export default {
  name: 'App',
  components: {
    Historia,
    Opciones
  },
  data() {
    return {
      datos: {
        text: "La historia comienza con un pequeño byte, el cual tiene dos opciones para seguir su camino.",
        opciones: {
          A: "opción 0",
          B: "opción 1"
        }
      }
    }
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

* {
  margin: 0;
  padding: 0;
  list-style: none;
  box-sizing: border-box;
  text-decoration: none;
}
</style>
