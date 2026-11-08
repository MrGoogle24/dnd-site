<script setup lang="ts">
defineProps<{
  name: string
  /*  level: number
  castingTime: string
  range: string
  components: string
  duration: string
  school: string
  save: string
  damage: string
  effect: string */
}>()
</script>

<template>
  <div id="spell-minimised">
    <button id="maximise-spell">
      {{ name }}
    </button>
  </div>
  <div id="spell-maximised"></div>
</template>

<style>
#maximise-spell {
  background-color: red;
}
</style>
