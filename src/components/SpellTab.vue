<script setup lang="ts">
defineProps<{
  spellName: string
  /*  spellLevel: number
  spellCastingTime: string
  spellRange: string
  spellComponents: string
  spellDuration: string
  spellSchool: string
  spellAttackType: string */
}>()
</script>

<template>
  <div id="spell-minimised">
    <button id="maximise-spell">
      {{ spellName }}
    </button>
  </div>
  <div id="spell-maximised"></div>
</template>

<style></style>
