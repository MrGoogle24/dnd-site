<script setup lang="ts">
import { ref, computed } from 'vue'

const searchItem = ref('')

const spells = ['fireball', 'magic missile', 'fire bolt']

const serachResult = computed(() => {
  return spells.filter((spell) => {
    if (spell.includes(searchItem.value)) {
      return true
    } else {
      return false
    }
  })
})
</script>

<template>
  <input v-model="searchItem" placeholder="Search..." />
  <ul>
    <li v-for="spell in serachResult" :key="spell">{{ spell }}</li>
  </ul>
</template>

<style></style>
