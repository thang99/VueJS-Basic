<template>
  <div id="product__detail">
      <h4>{{product.name}}</h4>
      <p>Price: {{product.price}} VND</p>
  </div>
</template>

<script>
export default {
    name:'ProductDetail',
    props:['product']
}
</script>

<style>
#product__detail {
    border: 1px solid black;
    padding:10px;
    text-align: center;
    background-color: lawngreen;
}

</style>