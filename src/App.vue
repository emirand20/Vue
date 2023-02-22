<template>
  <h1>Vue</h1>
  <hr />
  <!--<span v-text="'Hola mundo'"></span>-->
  <h2>Tu edad es: {{ edad }}</h2>
  <h3 v-show="edad >= 18 ">Eres mayor</h3>
  <span v-show="edad < 18 ">Eres menor</span>

  <!--<div v-html="html">
  </div>-->
</template>

<script>
export default {
  data(){
    return{
      edad: 19,
      //html: '<h3>hola</h3>'
    }
  }
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Lato&display=swap');

body {
  text-align: center;
  background-color: #4C566A;
  font-family: 'Lato', sans-serif;
  color: white;
}
</style>