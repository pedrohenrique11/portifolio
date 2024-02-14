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
  </footer>
</template>

<style scoped>
  .content {
    margin-top: 2rem;
  }
  footer p {
    text-align: center;
  }
</style>
