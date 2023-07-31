<script setup>
import TablaHeader from './TablaHeader.vue';
import TablaFila from './TablaFila.vue';
// propiedades como un listado
//let propiedades = defineProps(['productos','colorfondo','colortexto']); // propiedades.productos 
const propiedades=defineProps({
    productos:{default:[]},
    colorfondo:{default:'yellow'},
    colortexto:{default:'black'}
});
propiedades.productos.forEach(
  (value,index) => value.subTotal=value.cantidad*value.precioUnitario
);

</script>
<template>
  <table border="1">
    <TablaHeader/>
    <tbody>
      <tr v-for="alias in propiedades.productos">
        <TablaFila :alias="alias" :colorfondo="propiedades.colorfondo" :colortexto="propiedades.colortexto"  />
      </tr>
    </tbody>
  </table>
</template>
<style>
</style>