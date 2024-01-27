<script setup lang="ts">
import { ref } from 'vue'
const myObj = {
  title: 'My Name',
  age: 55
}

const ageIncrease = ref(0)
const nameChange = ref('My Name')
const title = myObj.title
</script>

<template>
  <h1>Vue Component</h1>
  <p>{{ ageIncrease }}</p>
  <button @click="ageIncrease++">Age +</button>
  <button @click="ageIncrease--">Age Decrease</button>

  <div class="title" @click="nameChange = 'Changed'">{{ nameChange }}</div>
</template>

<style scoped>
h1,
.title {
  /* padding-top: 10rem; */
  font-size: 3rem;
}
</style>
