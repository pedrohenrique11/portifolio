<script setup>
import { RouterView } from 'vue-router'
import MenuMobile from './components/MenuMobile.vue';
import TheHeader from './components/TheHeader.vue';

</script>

<template>
  <TheHeader />
  <MenuMobile />
  <div class="content">
    <RouterView />
  </div>
  <footer>
    <p>© 2005-2021 Pedro Henrique</p>
  </footer>
</template>

<style scoped>
  .content {
    margin-top: 2rem;
  }
  p {
    text-align: center;
  }
</style>
