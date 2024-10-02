<template>
  <div>
    <h1>Bài3</h1>
    <h3>Ngày sinh: {{inputValue}}</h3>
    <input type="date" v-model="inputValue">
  </div>
</template>

<script setup>
import{ref} from "vue"
const inputValue = ref("")
</script>

<style>

</style>