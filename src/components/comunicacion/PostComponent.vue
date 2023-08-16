<template>
  <div class="card">
    <div class="card-header">
      <h3>{{ props.title }}</h3>
    </div>
    <div class="card-body">
      <p>{{ props.content }}</p>
      <input type="text" name="" id="" placeholder="Ingrese su nombre" v-model="mensaje" >
      <button @click="handleClick" >Enviar</button>
    </div>
  </div>
</template>

<script setup>

  import {ref, defineProps, defineEmits} from 'vue'

  const props = defineProps({
    title : {
      type : String,
      required : true
    },
    content : {
      type : String,
      default : 'Este es un texto por default'
    },
    number : {
      type : Number,
      required : true
    }
  });

  const emit = defineEmits(['sayHi'])
    
  let mensaje = ref('');

  const handleClick = () => {
    emit("sayHi", mensaje.value + ' (enviado desde componente número : ' + props.number + ')')
  }


</script>

<style scoped>
  .card{
    margin: 10px;
  }
</style>