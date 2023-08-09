<template>
    <form @submit.prevent="manejarEntrada" action="post">
        <label for="texto">Ingrese su nombre</label>
        <input v-model="entradaTexto" name="texto" type="text">
        <button type="submit">OK</button>
    </form>
</template>

<script setup>

let entradaTexto = "";

function manejarEntrada(){
    console.log(entradaTexto);
}

</script>

<style></style>