<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <button @click="count++">click me!</button>
  <p>you have clicked the button above {{ count }} times.</p>
</template>

<style></style>
