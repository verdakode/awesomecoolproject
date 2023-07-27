<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ items: any }>()

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
