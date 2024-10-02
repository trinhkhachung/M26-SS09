<template>
  <div>
    <h1>Bài 7</h1>
    <h2>Thêm mới sản phẩm</h2>
    <form @submit.prevent="handleClick">
        <label for="productId">mã sản phẩm</label> <br>
        <input  id="productId" v-model="products.productId" type="text" required ><br>

        <label for="productName">Tên sản phẩm</label><br>
        <input  id="productName" v-model="products.productName" type="text" required><br>

        <label for="price">giá</label><br>
        <input id="price" v-model="products.price" type="number" required><br>
        
        <label for="quantity">số lượng</label><br>
        <input  id="quantity" v-model="products.quantity" type="number" required><br>

        <button type="submit"> thêm mới</button>
    </form>
  </div>
</template>

<script setup>
import {reactive} from 'vue'
const products = reactive({
    productId: '',
    productName: '',
    price: 0,
    quantity: 0,
})
function handleClick() {
    console.log('Products: ',products);
    products.productId = '';
    products.productName = '';
    products.price = 0;
    products.quantity =0;
    
}
</script>

<style>

</style>