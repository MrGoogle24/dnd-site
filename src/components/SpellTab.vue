<script setup lang="ts">
defineProps<{
  name: string
  level: number
  castingTime: string
  /* range: string
  components: string
  duration: string
  school: string
  save: string
  damage: string
  effect: string*/
}>()
</script>

<template>
  <div class="spell-minimised">
    <button class="maximise-spell">
      <span class="spell-level">
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
      </span>
      <span class="spell-info">
        <span class="spell-name"> {{ name }} </span> <br />
        <span class="spell-castingTime"> {{ castingTime }} </span>
      </span>
    </button>
  </div>
  <div class="spell-maximised" hidden></div>
</template>

<style>
.maximise-spell {
  background-color: #181818;
  border-radius: 2px;
  border-color: hsla(200, 100%, 37%, 0.2);
  text-align: left;
  color: #aaa;
  display: flex;
  gap: 1rem;

  width: 100%;
  padding: 0.75rem 1rem;
}

.spell-level {
  color: aquamarine;
  width: 6rem;
  text-align: center;
  flex-shrink: 0;
}
</style>
