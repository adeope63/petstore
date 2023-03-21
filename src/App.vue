<template lang="">
  <div id="app">
    <header>
      <h1>{{sitename}}</h1>
      <button @click='showCheckout'>{{this.cart.length}} Checkout</button>
    </header>
  </div>
</template>

<script>
export default {
  name: 'App',
  components:{

  },
  data() {
    return { 
      sitename:'Vue.js Pet Store',
      cart: []
    }
  },
  methods:{showCheckout(){} }
}
</script>
<style lang="">
  
</style>