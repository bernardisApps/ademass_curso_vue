<template>
    <h1 :class="{'danger':hasError}" >texto de prueba cambia de color segun : {{ hasError }}</h1>
    <button @click="invertir" >Cambiar</button>
</template>

<script setup>
    import {ref} from 'vue'
    let hasError = ref(true)
    function invertir(){
        hasError.value = !hasError.value;
    }
</script>

<style scoped>
    .danger{
        color: red;
    }
</style>