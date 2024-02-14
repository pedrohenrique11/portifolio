<script setup>
    import { RouterLink } from 'vue-router';
</script>

<template>
    <header>
      <h3>Pedro Henrique</h3>
        <nav>
          <RouterLink class="link" to="/">Home</RouterLink>
          <RouterLink class="link" to="/projects">Projects</RouterLink>
          <RouterLink class="link" to="/about">About</RouterLink>
        </nav>
        <ul>
          <li>
            <a href="https://github.com/pedrohenrique11" target="_blank"><img src="../components/icons/icons8-github.svg" alt=""></a>
          </li>
          <li>
            <a href="https://www.linkedin.com/in/pedro-henrique-79483b19a/" target="_blank"><img src="../components/icons/icons8-linkedin.svg" alt=""></a>
          </li>
        </ul>
  </header>
</template>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        
        border-bottom: 1px solid var(--secondary-color);
    }
    .link {
      color: #fff;
    }
    .link:hover {
      color: var(--secondary-color);
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