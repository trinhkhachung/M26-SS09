<template>
  <div>
    <h1>Bài 4</h1>
    <h3>Tiến độ hoàn thành: {{inputValue}}%</h3>
    <input type="range" v-model="inputValue">
  </div>
</template>

<script setup>
import {ref} from "vue"
const inputValue = ref("")
</script>

<style>

</style>