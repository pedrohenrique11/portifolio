<script setup>
import { RouterLink, RouterView } from 'vue-router'
import ButtonMenu from '../src/components/ButtonMenu.vue'
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
          <a href="https://github.com/pedrohenrique11"><img src="../src/components/icons/icons8-github.svg" alt=""></a>
        </li>
        <li>
          <a href="https://www.linkedin.com/in/pedro-henrique-79483b19a/"><img src="../src/components/icons/icons8-linkedin.svg" alt=""></a>
        </li>
      </ul>
  </header>
  <ButtonMenu></ButtonMenu>
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
    align-items: center;
    list-style: none;

    padding: 0;
  }
  li {
    margin: 0;
  }
  img {
    width: 35px;
  }
  a {
    margin: 0 0.4rem;
  }
  @media (max-width: 700px) {
    nav {
      display: none;
    }
  } 

</style>
