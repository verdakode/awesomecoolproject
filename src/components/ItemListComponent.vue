<script setup lang="ts">
import { ref } from 'vue'
import type { ItemInterface } from '../../components/items/Item.interface'

defineProps<{ items: ItemInterface }>()

const count = ref(0)
</script>

<template>
  <div class="card">
    <h3>Items:</h3>
    <ul>
      <li v-for="(item, index) in items" :key="item.id">
        {{ item.name }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
</style>
