<template>
  <div>
     <h1>Bài8</h1>
     <h2>Thêm mới người dùng</h2>
      <form @submit.prevent="addUser">
        <div>
          <label for="productId">họ và tên:</label> <br>
          <input id="productId" v-model="user.name" type="text" required />
        </div>
        
        <div>
          <label for="productName">email:</label> <br>
          <input id="productName" v-model="user.email" type="text" required />
        </div>
  
        <div>
          <label for="price">pass:</label><br>
          <input id="price" v-model="user.pass" type="password" required />
        </div>
  
        <div>
          <label for="quantity">rePass:</label> <br>
          <input id="quantity" v-model="user.rePass" type="password" required />
        </div>
  <br>
        <button type="submit">Đăng kí</button>
      </form>
  </div>
</template>

<script setup>
import { reactive } from 'vue';
const user = reactive({
          name: '',
          email: '',
          pass: '',
          rePass: ''
        }) 
     function addUser() {
        console.log('Product added:',user);
        user.name = '';
        user.email = '';
        user.pass = '';
        user.rePass = '';
      }
</script>

<style>

</style>