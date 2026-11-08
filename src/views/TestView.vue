<script setup lang="ts">
import SpellTab from '@/components/SpellTab.vue'
import spells from '@/assets/spells.json'
</script>

<template>
  <SpellTab v-for="spell in spells" :key="spell.name" spell-name="spell" />
</template>

<style></style>
