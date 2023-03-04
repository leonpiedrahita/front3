<script setup>
  const name = `vue dinamico`;
  const styleColor = "color: blue";
  const activo = false;

  const arrayFrutas = [
        {
            name: "Manzana",
            price: "$1.00",
            description: "Una manzana",
        },
        {
            name: "Pera",
            price: "$2.00",
            description: "Una pera",
        },
        {
            name: "Naranja",
            price: "$3.00",
            description: "Una naranja",
        },
    ];

</script>

<template>
  <h1>Hola {{name.toUpperCase()}}</h1>
  <h2 v-bind:style="styleColor"> Soy azul </h2>
  <h3 :style="styleColor"> Soy azul </h3>
   <h3> {{ activo ? "Estoy activo":"Estoy inactivo" }}</h3> <!--Operador ternario de comparacion -->
  
  <p v-if="activo === true">Estoy activo</p>
<p v-else-if="activo === false">Estoy inactivo</p>
<p v-else>Estoy indeciso</p>
<ul>
        <li v-for="fruta in arrayFrutas" 
        :key="fruta.name">
            {{ fruta.name }} - {{ fruta.price }} - {{ fruta.description }}
        </li>
    </ul>

</template>

<style>
h1 {
color:red;
}
</style>