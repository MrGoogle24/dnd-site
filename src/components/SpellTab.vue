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
  damage: string | null
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
          <span class="spell-attackMod">{{
            attackMod != null ? (attackMod > 0 ? '+' + attackMod : attackMod) : ''
          }}</span>
          <span class="spell-save">{{ save == null ? '' : save }}</span>
          <span class="spell-damage">{{ damage == null ? '' : damage }}</span>
          <span class="spell-effect">{{ effect == null ? '' : effect }}</span>
        </div>
      </span>
    </button>
  </div>
  <div class="spell-maximised" hidden></div>
</template>

<style scoped>
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
  width: 7ch;
  text-align: center;
  flex-shrink: 0;
}

.spell-info {
  flex: 1;
  min-width: 0; /* lets the text shrink so ellipsis can work */
}

.spell-name {
  display: block;
  font-size: 120%;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
}

.spell-sub-info {
  display: flex;
  gap: 0.75rem;
  font-size: 80%;
  color: #999;
}

.spell-sub-info span {
  min-width: 0;
  overflow: hidden;
  text-overflow: ellipsis;
  white-space: nowrap;
  text-align: center;
}

.spell-castingTime {
  width: 14ch;
}
.spell-range {
  width: 16ch;
}
.spell-components {
  width: 10ch;
}
.spell-duration {
  width: 14ch;
}
.spell-school {
  width: 13ch;
}
.spell-attackMod {
  width: 4ch;
}
.spell-save {
  width: 9ch;
}
.spell-damage {
  width: 9ch;
}
.spell-effect {
  width: 13ch;
}

@media (max-width: 600px) {
  .maximise-spell {
    gap: 0.5rem;
  }

  .spell-sub-info {
    flex-wrap: wrap;
    gap: 0.25rem 0.5rem;
  }

  .spell-sub-info span {
    min-width: 0;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    text-align: center;
  }

  .spell-sub-info span:empty {
    display: none;
  }

  .spell-school,
  .spell-components,
  .spell-duration {
    display: none;
  }
}
</style>
