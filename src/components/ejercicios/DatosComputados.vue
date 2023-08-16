<template>
  <div>
    <input type="text" name="" id="" v-model="mensaje">
    <h3>{{ reverse }}</h3>
  </div>
</template>

<script setup>
    import {ref, computed} from 'vue'
    let mensaje = ref('');
    const reverse = computed(()=>{
        return mensaje.value.split('').reverse().join('')
    })
</script>

<style scoped>

</style>