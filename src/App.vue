<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/test">Test!</RouterLink>
    </nav>
  </header>
  <RouterView />
</template>

<style scoped>
nav {
  display: flex;
  justify-content: center;
  gap: 1.5rem;
  padding: 1rem 0;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}
</style>
