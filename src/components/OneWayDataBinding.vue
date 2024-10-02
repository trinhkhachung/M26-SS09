<template>
 <div>
     <h1>
    One-way Data Binding 
  </h1>
  <h3>userName:{{userName}}</h3>
  <input type="text" :value="userNam">
  <button @click="handleChangeName">meo</button>
 </div>
</template>

<script setup>
import{ref} from "vue"
const userName = ref("Nguyễn Văn B");
const handleChangeName = () =>{
    userName.value = "nguyen văn a"
};

</script>

<style>

</style>