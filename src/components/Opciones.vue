<template>
    <section>
        <ul>
            <li v-for="opcion in opciones" :key="opcion.index">{{opcion.index}} {{opcion}}</li>
        </ul>
    </section>
</template>

<script>
export default {
    setup() {
        
    },
    props: {
        opciones: Object
    }
}
</script>