<script setup lang="ts">
import ItemListComponent from './components/ItemListComponent.vue'
import ItemInterface from './components/items/Item.ts'

const items: ItemInterface[]= [
  { id: 1,
    name: "Item 1",
    selected: false },
  { id: 2,
    name: "Item 2",
    selected: false },
  { id: 3,
    name: "Item 3",
    selected: false }
];
</script>

<template>
  <div class="home">
    <HelloWorld :items="items"/>
  </div>
</template>

<style scoped>
</style>
