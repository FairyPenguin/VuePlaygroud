<script setup lang="ts">
defineProps<{ descriptin: string }>()
</script>

<template>
  <h1>My first vue component</h1>
  <p>{{ descriptin }}</p>
</template>

<style>
h1 {
  font-size: 2rem;
}
</style>
