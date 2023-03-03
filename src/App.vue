<script setup>
  const name = `vue dinamico`;
  const styleColor = "color: blue";
</script>

<template>
  <h1>Hola {{name}}</h1>
  <h2 v-bind:style="styleColor"> Soy azul </h2>
</template>

<style>
h1 {
color:red;
}
</style>