<template>
    <h1 v-for="(nombre, index) in nombres" :key="index"> {{ nombre }} </h1>
</template>

<script setup>
    import {ref} from 'vue'
    let nombres = ref(['matias', 'bruno', 'florencia']);
</script>

<style scoped>

</style>