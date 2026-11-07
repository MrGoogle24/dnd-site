<script setup lang="ts">
import { ref } from 'vue'

const count = ref(0)
</script>

<template>
  <button @click="count++">You clikced me {{ count }} times!</button>
</template>

<style></style>
