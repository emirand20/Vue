<template>
  <div class="container mt-3">
    <Header /> 
    <Form />
  </div>
</template>

<script>
import Header from "./components/Header.vue"
import Form from "./components/Form.vue"

export default {
  components: {
    Header,
    Form
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

.contador {
  background-color: rgb(8, 99, 96);
  color: snow;
  font-weight: bold;
  height: 400px;
}
</style>