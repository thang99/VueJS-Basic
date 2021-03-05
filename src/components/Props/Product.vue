<template>
    <div>
        <h2>Product List</h2>
        <div id="product">
            <ProductDetail v-for="product in products" :key="product.id" :product="product" />
        </div>
    </div>
 
</template>

<script>
import ProductDetail from './ProductDetail'

export default {
    name:'Product',
    components: {
        ProductDetail,
    },
    data() {
        return {
            products: [
                {id:1, name:'Sam Sung Galaxy J2 Prime', price:26000000},
                {id:2, name:'Iphone X', price:10000000},
                {id:3, name:'Realme C1', price:2500000}
            ]
        }
    },
}
</script>

<style>
#product {
    display: flex;
    justify-content: space-around;
}
h2 {
    text-align: center;
    margin-bottom: 50px;
    color: blue;
}
</style>