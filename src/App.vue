<script setup>
  const name = `vue dinamico`;
  const styleColor = "color: blue";
  const activo = false;
</script>

<template>
  <h1>Hola {{name.toUpperCase()}}</h1>
  <h2 v-bind:style="styleColor"> Soy azul </h2>
  <h3 :style="styleColor"> Soy azul </h3>
   <h3> {{ activo ? "Estoy activo":"Estoy inactivo" }}</h3> <!--Operador ternario de comparacion -->
</template>

<style>
h1 {
color:red;
}
</style>