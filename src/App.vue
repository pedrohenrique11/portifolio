<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <h1>Pedro Henrique</h1>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/about">About</RouterLink>
      </nav>
  </header>

  <RouterView />
</template>

<style scoped>
  header {
    display: flex;
    justify-content: space-evenly;
    justify-content: center;
  }
</style>
