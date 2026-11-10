<script setup lang="ts">
defineProps<{
  name: string
  level: number
  /* castingTime: string
  range: string
  components: string
  duration: string
  school: string
  save: string
  damage: string
  effect: string*/
}>()
</script>

<template>
  <div id="spell-minimised">
    <button id="maximise-spell">
      {{
        level == 0
          ? 'Cantrip'
          : level == 1
            ? '1st'
            : level == 2
              ? '2nd'
              : level == 3
                ? '3rd'
                : level + 'th'
      }}
      {{ name }}
    </button>
  </div>
  <div id="spell-maximised" hidden></div>
</template>

<style>
#maximise-spell {
  background-color: #181818;
  border-radius: 2px;
  border-color: hsla(200, 100%, 37%, 0.2);
  text-align: left;
  color: #aaa;

  width: 100%;
  height: 20%;
}
</style>
