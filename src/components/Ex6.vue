<template>
  <div>
    <h1>Bài6</h1>
    <h3>Sở thích: {{check}}</h3>
    <input type="checkbox" id="code" value="code" v-model="check">
    <label for="code">code</label>
    <br>
    <input type="checkbox" id="play" value="playgem" v-model="check">
  <label for="play">playgem</label>
    <br>
  <input type="checkbox" id="playchess" value="cờ vua" v-model="check">
  <label for="playchess">cờ vua</label>
  </div>
</template>

<script setup>
import {ref} from "vue"
const check = ref([])
</script>

<style>

</style>