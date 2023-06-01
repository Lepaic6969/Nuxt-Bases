<template>
    <div>
      <h1>Error Encontrado</h1>
      <h3>{{ error.statusCode }} - {{ error.statusMessage }}</h3>
      <button @click="handleError">Limpiar Errores</button>
    </div>
</template>
<script setup>
  const route=useRoute();

  // Aquí recibimos las props de este componente, se generar como props en este componente las causales del error...
  const props=defineProps({
    error:Object
  });
  const {error}=props; //Aquí desestructuro el objeto de error que se generó (Lo puede también hacer de forma directa).

  //Aquí va la lógica del botón.
  //Me redirije o al inicio o a la última ventana que visité entes de caer en el error, si esta última era correcta.
  const path=(route.path===error.url)?"/":route.path;
  const handleError=()=>{
    //Me borra los errores y me redirije a donde le diga.
    clearError({redirect:path});
  }
</script>

<style scoped>
    div{
        text-align: center;
    }
</style>