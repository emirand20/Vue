<template>
  <div class="container">
    <h1>Cotizador de Criptomonedas</h1>
    <grid>
      <formulario @info-monedas="get" />
      <Data :cripto="info.cripto" />
    </grid>
  </div>
</template>

<script>
import Formulario from "./components/Formulario.vue";
import Data from "./components/Data.vue";
import GridVue from "./components/Grid.vue";
import Grid from "./components/Grid.vue";

export default {
  components: { Formulario, Data, Grid },
  data: () => ({
    info: {
      cripto: '*',
      moneda: '*',
      img: '',
      price: 0,
    }
  }),
  methods: {
    async get(cripto, moneda) {
      const res = await fetch(
        `https://min-api.cryptocompare.com/data/pricemultifull?fsyms=${encodeURI(cripto)}&tsyms=${encodeURI(moneda)}`
      )
      const data = await res.json()
      console.log(data)
    },

  },
};
</script>