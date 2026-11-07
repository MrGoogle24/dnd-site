<script setup lang="ts">
import FloatingButtons from 'vue-floating-buttons'
Vue.component('FloatingButtons', FloatingButtons)
</script>

<template>
  <div id="test">
    <FloatingButtons :buttons="buttons" />
  </div>
</template>

<style></style>
