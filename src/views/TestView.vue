<script setup lang="ts">
import SpellTab from '@/components/SpellTab.vue'
import spells from '@/assets/spells.json'
</script>

<template>
  <div class="spell-list">
    <SpellTab v-for="spell in spells" :key="spell.name" v-bind="spell" />
  </div>
</template>

<style>
.spell-list {
  gap: 4%;
}
</style>
