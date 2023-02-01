<script>
export default {
  data: () => ({
    contador: 0,
  }),
  methods: {
    suma() {
      ++this.contador;
    },
    resta() {
      this.contador--;
    },
    reset() {
      this.contador = 0;
    },
  },
};
</script>
<template>
  <div class="container">
    <img src=./assets/logo.svg alt="logo vue" width="125" height="125 "/>
    <small>
      <h1>Hola mundo desde Vue.js 3</h1>
    </small>
    <hr />

    <h2>Contador {{ contador }}</h2>
    <button @click="suma">+1</button>
    <button @click="resta">-1</button>V
    <button @click="reset">reset</button>
  </div>
</template>

<style scoped>
small {
  color: #666;
}
h1 {
  font-weight: bolder;
}
h2 {
  font-size: 2.5rem;
}
button {
  cursor: pointer;
  font-size: 1rem;
  margin: 0px 5px;
}
</style>