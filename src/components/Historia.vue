<template>
    <h2>{{msg}}</h2>
    <hr>
    <p>{{ Historia }}</p>
</template>

<script>
export default {
    setup() {
        
    },
    data () {
        return {  }
    },
    props: {
        Historia: Object,
        msg: String
    }
}
</script>