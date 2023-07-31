<script setup>
    const propiedades = defineProps(['alias','colorfondo','colortexto']); // defineProps lee las propiedades que el padre envio al hijo
</script>
<template>
        <td class="fila">{{ propiedades.alias.id }} </td>
        <td class="fila">{{ propiedades.alias.nombre }}</td>
        <td class="fila">{{ propiedades.alias.cantidad }}</td>
        <td class="fila">{{ propiedades.alias.precioUnitario.toLocaleString("es-ES") }}</td>
        <td class="fila">{{ propiedades.alias.subTotal.toLocaleString("es-ES") }}</td>
</template>
<style scoped>
    .fila  {
        background-color: v-bind('propiedades.colorfondo');
        color:v-bind('propiedades.colortexto')
    }
</style>