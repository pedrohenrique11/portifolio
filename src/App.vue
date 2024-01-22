<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <h3>Pedro Henrique</h3>
      <nav>
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/projects">Projects</RouterLink>
      </nav>
      <ul>
        <li>
          <a href=""></a>
        </li>
        <li>
          <a href=""></a>
        </li>
      </ul>
  </header>

  <RouterView />
</template>

<style scoped>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;

    border-bottom: 1px solid hsla(160, 100%, 37%, 1);
  }
  nav {
    padding: 1rem 2rem;
  }
  h3 {
    font-size: 1.4rem;
  }
  ul{
    display:flex;
    list-style: none;
  }
</style>
