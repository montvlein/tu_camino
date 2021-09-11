<template>
  <div>
    <img alt="Vue logo" src="./assets/bird.gif">
    <Historia msg="Bienvenido a tu cAPPmino" :Historia="state.historiaActual().historia"/>
    <!-- <Opciones :opciones="state.historiaActual().opciones" :changeEvent="handleClick()"/> -->
    <section>
      <h4>Opciones</h4>
      <ul>
        <li v-for="(opcion, index) in state.historiaActual().opciones" :key="opcion.index">
          <button @click="handleClick(index)">{{ index }}</button>{{ opcion }}
        </li>
      </ul>
    </section>
  </div> 
</template>

<script>
import Historia from './components/Historia'
// import Opciones from './components/Opciones'
import eventos from './data/data.json'

export default {
  name: 'App',
  components: {
    Historia,
    // Opciones
  },
  data() {
    return {
      state: {
        ultimaOpcion: "",
        contador:1,
        historiaActual: () => { return eventos.find( (evento) => evento.id === this.state.contador + this.state.ultimaOpcion.toLowerCase() )}
      },
      eleccion: ''
    }
  },
  methods: {
    handleClick (opcionElegida) {
      if (this.state.contador < 5) {
        this.state.ultimaOpcion = opcionElegida;
        this.state.contador += 1;
      } else {
        alert("FIN?");
        window.location.reload();
      }
    },
  },
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
