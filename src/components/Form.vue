<template lang="">
    <div>
        <h2>Checkout</h2>
        <h3>Added products</h3>
        <div v-for='(product,index) in cart' :key='index'>
            {{ product.id}} <button @click="cart.splice(index,1)">remove</button>
        </div>
        <p>
            <strong>Name</strong> <input v-model="name" type="text">
            <strong>Address</strong> <input v-model="address" type="text">
            <button>Submit</button>

        </p>
    </div>
</template>

<script>
export default {
    /* eslint-disable */
    name:"Form",
    props: ['cart'],
    data(){
        return {
            name: "",
            address: "",
        }
    }
}
</script>
<style lang="">
    
</style>