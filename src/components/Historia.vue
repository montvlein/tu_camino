<template>
    <section>
        <h2>{{msg}}</h2>
        <hr>
        <p>{{ Historia }}</p>
    </section>
</template>

<script>
export default {
    setup() {
        
    },
    data () {
        return {  }
    },
    props: {
        Historia: String,
        msg: String
    }
}
</script>