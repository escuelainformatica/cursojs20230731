<script setup>
import Tabla from './componentes/Tabla.vue';
const productos = [
  { id: 1, nombre: "cocacola",cantidad:100,precioUnitario:2000 },
  { id: 2, nombre: "fanta",cantidad:50,precioUnitario:1800 },
  { id: 3, nombre: "sprite",cantidad:25,precioUnitario:2100 },
];
// forEach, map, reduce
/*
productos.forEach(
  function (value,index) { 
    value.subTotal=value.cantidad*value.precioUnitario;
    //productos[index].subTotal=productos[index].cantidad*productos[index].precioUnitario;
  }
);
*/




const celulares = [
  { id: 1, nombre: "apple",cantidad:100,precioUnitario:2000 },
  { id: 2, nombre: "samsung",cantidad:100,precioUnitario:2000 },
  { id: 3, nombre: "lg",cantidad:100,precioUnitario:2000 },
];    
</script>

<template>
  <Tabla :productos="productos" colorfondo="red" colortexto="white" />
  <br>
  <Tabla :productos="celulares" colorfondo="blue" colortexto="white" />
  <br>
  <Tabla :productos="celulares" />
</template>

<style scoped></style>
