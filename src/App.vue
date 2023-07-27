<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'

const items: any[]= [
  { id: 1,
    name: "Item 1" },
  { id: 2,
    name: "Item 2" },
  { id: 3,
    name: "Item 3" }
];
</script>

<template>
  <div class="home">
    <HelloWorld :items="items"/>
  </div>
</template>

<style scoped>
</style>
