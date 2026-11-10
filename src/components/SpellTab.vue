<script setup lang="ts">
defineProps<{
  name: string
  level: number
  castingTime: string
  range: string
  components: string
  duration: string
  school: string
  attackMod: number | null
  save: string | null
  damage: string
  effect: string | null
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
        <span class="spell-name">{{ name }}</span> <br />
        <div class="spell-sub-info">
          <span class="spell-castingTime">{{ castingTime }}</span>
          <span class="spell-range">{{ range }}</span>
          <span class="spell-components">({{ components }})</span>
          <span class="spell-duration">{{ duration }}</span>
          <span class="spell-school"> {{ school }} </span>
          <span class="spell-attackMod">{{ attackMod ? '+' + attackMod : '' }}</span>
          <span class="spell-save">{{ save == null ? '' : save }}</span>
          <span class="spell-damage">{{ damage }}</span>
          <span class="spell-effect">{{ effect == null ? '' : effect }}</span>
        </div>
      </span>
    </button>
  </div>
  <div class="spell-maximised" hidden></div>
</template>

<style>
@media (max-width: 600px) {
  .spell-school,
  .spell-components,
  .spell-duration {
    display: none;
  }

  .maximise-spell {
    background-color: #181818;
    border-radius: 2px;
    border-color: hsla(200, 100%, 37%, 0.2);
    text-align: left;
    color: #aaa;
    display: flex;
    gap: 0.3rem;

    width: 100%;
    padding: 0.75rem 1rem;
  }

  .spell-sub-info {
    display: flex;
    gap: 0.3rem;

    font-size: 80%;
    color: #999;
  }
}

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
  width: 4rem;
  text-align: center;
  flex-shrink: 0;
}

.spell-name {
  font-size: 120%;
}

.spell-sub-info {
  display: flex;
  gap: 1rem;

  font-size: 80%;
  color: #999;
}
</style>
