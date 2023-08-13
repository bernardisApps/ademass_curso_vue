<template>
    <form>
        <input v-model="inputText" type="text" name="nombre" id="">
        <br>
        <input v-model="inputCheck" type="checkbox" name="" id=""> Acepto los términos y condiciones
        <br>
        <select v-model="inputOption" name="" id="">
            <option value="Spain">Spain</option>
            <option value="Uk">Uk</option>
            <option value="Italy">Italy</option>
        </select>
    </form>
    <h3>{{ inputText }}</h3>
    <h3> {{ inputCheck }} </h3>
    <h3>{{ inputOption }}</h3>
</template>

<script setup>
    import {ref} from 'vue'
    let inputText = ref('')
    let inputCheck = ref(true)
    let inputOption = ref('Spain')
</script>

<style scoped>

</style>