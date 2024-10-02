<template>
  <div>
    <h1>Bài 1</h1>
    <h2>email</h2>
    <input type="text" v-model="inputValue">
    <h3>input value: {{inputValue}}</h3>
  </div>
</template>

<script setup>
    import{ref} from "vue"
    const inputValue = ref("Rikkei academy")
</script>

<style>

</style>