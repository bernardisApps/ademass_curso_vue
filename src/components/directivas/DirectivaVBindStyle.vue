<template>
    <p :style="{backgroundColor:bg, color:'white'}" >Párrafo de prueba</p>
    <button class="btn btn-outline-success" @click="manejadorClick" :title="title" >Cambiar color</button>
</template>

<script setup>
    import {ref} from 'vue'
    let bg = ref('grey');
    let title = ref('Cambiar el color del fondo');
    const manejadorClick = () => {
        if (bg.value === "grey"){
            bg.value = "black";
        }else{
            bg.value = "grey";
        }
    }
</script>

<style scoped>

</style>