<script setup lang="ts">
import { ref } from 'vue'
import type { ItemInterface } from '../../components/items/Item.interface'

defineProps<{ items: ItemInterface }>()

const emit = defineEmits<{
  (e: 'selectItem', id: number): any
}>()

const count = ref(0)

const handleClick = (item: ItemInterface) => {
  item.selected = !item.selected
  console.log('handleItemClick', item.id, item.selected)
}
</script>

<template>
  <div class="card">
    <h3>Items:</h3>
    <ul>
      <li v-for="(item, index) in items" :key="item.id" @click="handleClick(item)">
        {{ item.name }} [{{ item.selected }}]
      </li>
    </ul>
  </div>
</template>

<style scoped>
</style>
