<template>
  <div>
    <h1>Bài2</h1>
    <h2>email</h2>
    <input type="color" v-model="inputValue">
    <h3>mã màu: {{inputValue}}</h3>
  </div>
</template>

<script setup>
    import{ref} from "vue"
    const inputValue = ref("")
</script>

<style>

</style>