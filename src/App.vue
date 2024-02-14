<script setup>
import { RouterView } from 'vue-router'
import MenuMobile from './components/MenuMobile.vue';
import TheHeader from './components/TheHeader.vue';

</script>

<template>
  <TheHeader />
  <MenuMobile />
  <div class="content">
    <Transition
     enter-active-class="animate__animated animate__fadeInLeft" 
     leave-active-class="animate__animated animate__fadeOutLeft"
     mode="out-in">
      <RouterView />
    </Transition>
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
