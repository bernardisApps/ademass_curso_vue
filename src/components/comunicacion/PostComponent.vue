<template>
  <div class="card">
    <div class="card-header">
      {{ title }}
    </div>
    <div class="card-body">
      {{ content }}
    </div>
  </div>
</template>

<script>

  export default{
    name:'PostComponent',
    props:{
      title : {
        type : String,
        required : true,
        default : 'Título por default',
      },
      content : {
        type:String,
        required : true,
        default:'contenido por default'
      }
    },
    setup(){

      return{
      
      }
    }
  }

</script>

<style scoped>
  .card{
    margin: 10px;
  }
</style>