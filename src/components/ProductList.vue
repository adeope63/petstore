<template lang="">
    <main>
        <div v-for='product in products' :key="product.id">
            <h2>{{product.title}}</h2>
            <figure>
                <img v-bind:src="product.image" alt="">
            </figure>
            <p v-html='product.description'></p>
            <p>Price: {{product.price}}</p>
            <p>Available Stock: {{product.availableInventory}}</p>
            <button @click='addProduct(product)'>Add to cart</button>
        </div>
    </main>
</template>

<script>
export default {
    name:"productList",
    data(){
        return{
        products:[
            {
                id: 1001,
                title: "Cat Food, 25lb bag",
                image: "new.png",
                price: 100,
                availableInventory: 5
            }
        ]}
    },
    methods: {
        addProduct(product) {
            this.$emit('addProduct', product)
        }
    }
}
</script>
<style lang="">
    
</style>