<template>
  <div>
    <h1>Bài5</h1>
    <h3>Giới tính {{gender}}</h3>
    <input type="radio" id="male" value="Nam" v-model="gender" />
    <label for="male">nam</label>

     <input type="radio" id="feMale" value="Nử" v-model="gender" />
    <label for="feMale">nữ</label>

     <input type="radio" id="other" value="LGBT" v-model="gender" />
    <label for="other">khác</label>
  </div>
</template>

<script setup>
    import {ref} from "vue"
    const gender = ref("Nam")
</script>

<style>

</style>