<script setup>
const name = "Vue 3"
const styleColor = "color: green"
</script>

<template>
  <div>
  <h1>Esto es {{name}}</h1>
  <h2 v-bind="styleColor">Este texto es de color verde</h2>
  </div>
</template>
<style>
h1{
  color: red
}
</style>