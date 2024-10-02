<template>
  <div>
    <h1>Bài 9</h1>
    <h2>Đăng kí tài khoản</h2>
    <form @submit.prevent="addUser">
    <div>
        <label for="name">Tên sinh viên</label> <br>
        <input type="text" v-model="user.name" id="name">
    </div>
    <div>
        <label for="email">email</label> <br>
        <input type="email" v-model="user.email" id="email">
    </div>
    <div>
        <label for="password">Mật khẩu</label> <br>
        <input type="password" v-model="user.password" id="password">
    </div>
    <div>
        <label for="phoneNumber">Số điện thoại</label> <br>
        <input type="number" v-model="user.phoneNumber" id="phoneNumber">
    </div>
    <button type="submit">Đăng kí</button>
    </form>
    <p v-if="successMessage" style="color: green">{{ successMessage }}</p>
      <p v-if="errorMessage" style="color: red">{{ errorMessage }}</p>
  </div>
</template>

<script setup>
import {reactive, ref} from 'vue'
const user = reactive({
    name: '',
    email: '',
    password: '',
    phoneNumber: '',
});
function addUser() {
    if (!user.name || !user.email || !user.password ){
        errorMessage.value = 'điền đầy đủ vào cu';
        succesMessage.value = '';
        return;
    }
    const storedUsers = JSON.parse(localStorage.getItem(users)) || [];
    const emailExists = storedUsers.some(storedUser => storedUser.email === user.email);
    if (emailExists) {
      errorMessage.value = 'Email đã tồn tại!';
      successMessage.value = '';
      return;
    }
    storedUsers.push({ ...user });
    localStorage.setItem('users', JSON.stringify(storedUsers));
  
    successMessage.value = 'Đăng ký tài khoản thành công!';
    errorMessage.value = '';
  
    user.name = '';
    user.email = '';
    user.password = '';
    user.phoneNumber = '';
}
</script>

<style>

</style>