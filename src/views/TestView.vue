<script setup lang="ts">
import SpellTab from '@/components/SpellTab.vue'
import spells from '@/assets/spells.json'
</script>

<template>
  <div class="spell-list">
    <SpellTab class="spell" v-for="spell in spells" :key="spell.name" v-bind="spell" />
  </div>
</template>

<style>
.spell {
  padding: 5%;
}
</style>
