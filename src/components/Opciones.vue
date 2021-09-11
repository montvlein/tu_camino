<template>
  <section>
    <h4>Opciones</h4>
    <ul>
      <li v-for="(opcion, index) in opciones" :key="opcion.index">
        <button @click="changeEvent(index)">{{ index }}</button>{{ opcion }}
      </li>
    </ul>
  </section>
</template>

<script>
export default {
  setup() {},
  props: {
    opciones: Object,
    changeEvent: Function
  }
};
</script>