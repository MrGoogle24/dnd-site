<script setup lang="ts">
import { computed } from '@vue/reactivity';
import { ref } from 'vue'

const searchItem = ref('')

const spells = ['fireball', 'magic missile', 'fire bolt']

const serachResult = computed() => {
  return spells.filter((spell) => {
    spells.includes(spell.toLowerCase())
  })
}
</script>

<template>
  <input v-model="searchItem" placeholder="Search..." />
  <ul>
    <li v-for="spell in serachResult" :key="spell">{{ spell }}</li>
  </ul>
</template>

<style></style>
