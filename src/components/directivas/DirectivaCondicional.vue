<template>
    <h1 v-if="edad < 18">Eres menor de edad</h1>
    <h1 v-else>Eres mayor de edad</h1>
    <!--Cuando se tienen que renderizar muy seguido es mejor usar v-show-->
    <h1 v-show="edad < 18">Eres menor de edad</h1>
    <h1 v-show="edad >= 18" >Eres mayor de edad</h1>
</template>

<script setup>
    import {ref} from 'vue'
    let edad = ref(10);
</script>

<style scoped>

</style>