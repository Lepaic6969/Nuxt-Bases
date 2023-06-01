<template>
  <div>
    <Title>Post {{ id }}</Title>
    <!-- Esta es una primera forma de hacerlo -->
    <!-- <h2>Bienvenido al Post nº {{ $route.params.id }}</h2> -->
    <h2>Bienvenido al Post nº {{ id }}</h2>
  </div>
</template>
<script setup>

const {id}=useRoute().params;

/*  //Vamos a hacer validaciones en la ruta para que el id que me pasen sea estrictamente numérico.
    definePageMeta({
        validate:async(route)=>{
            return /^\d+$/.test(route.params.id);
        }
    }); */

  
//Vamos a generar códigos y mensajes de error personalizados. Es exactamente el mismo ejemplo
//que el que está arriba , sólo que con código y mensaje personalizado.
definePageMeta({
        validate:async(route)=>{
          if(! /^\d+$/.test(route.params.id)){
              throw createError({statusCode:'500',statusMessage:'Param Type is Invalid'});
          }
          return true;
        }
});



</script>

