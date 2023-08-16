<template>
  <div>
    <form action="">
      <input ref="element" v-model="producto.nombre" type="text" name="" id="" placeholder="ingrese nombre producto">
      <br>
      <input v-model="producto.precio" type="number" name="" id="" placeholder="Ingrese precio">
      <br>
      <button @click.prevent="handleClick" >Agregar</button>
    </form>
    <hr>
    <div class="table">
      <thead>
        <tr>
          <th>Nombre</th>
          <th>Precio</th>
          <th>Opciones</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(item, index) in productos" :key="index">
          <td>{{ item.nombre }}</td>
          <td>{{ item.precio }}</td>
          <td><button class="btn btn-outline-danger" @click="eliminarItem(index)" >Eliminar</button></td>
        </tr>
      </tbody>
    </div>
    <hr>
    <h2>Subtotal</h2>
    <p>{{subtotal}}</p>
    <h2>Total (con impuestos)</h2>
    <p>{{total}}</p>
  </div>
</template>

<script setup>
    import {ref, computed} from 'vue'
    const element = ref(null);
    const iva = 0.21;
    let productos = ref([]);
    const producto = ref({
        nombre : '',
        precio : 0
    })

    const handleClick = () => {
      productos.value.push({
        nombre : producto.value.nombre,
        precio : producto.value.precio
      })
      producto.value.nombre = '';
      producto.value.precio = '';
      element.value.focus();
    }

    let subtotal = computed(()=>{
      let suma = 0;
      productos.value.forEach(element => {
        suma+=element.precio
      });
      return suma;
    })

    let total = computed(() => {
      let porcentaje = subtotal.value * iva
      return subtotal.value + porcentaje;
    })

    const eliminarItem = (index) => {
      productos.value.splice(index,1);
    }

</script>

<style scoped>

</style>