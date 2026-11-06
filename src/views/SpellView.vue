<script setup lang="ts">
import { ref } from 'vue'

const name = ref('')
</script>

<template>
  <input v-model="name" placeholder="Your Name" />
  <p>Hello {{ name }}</p>
</template>

<style></style>
