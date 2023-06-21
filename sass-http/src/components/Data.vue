<template>
  <div class="data">
    <h2>Informacion ...</h2>
    <h3>
      <span class="cripto">BTC</span> - <span class="moneda">USD</span>
    </h3>
    <p>
      <img src="https://www.cryptocompare.com/media/37746238/eth.png" alt="">
      Precio: <strong>$300</strong>
    </p>
  </div>
</template>

<script>
export default {
  props: {
    cripto:{
      type: String,
      required: true
    },
    moneda:{
      type: String,
      required: true
    },
    img:{
      type: String,
      required: true
    },
    price:{
      type: String,
      required: true
    },
  }
};
</script>