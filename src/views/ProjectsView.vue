<script setup>
import TextSection from '../components/TextSection.vue'
import MyProjects from '../components/MyProjects.vue'
</script>
<template>
  <TextSection 
  title='My Projects'
  />
  <MyProjects></MyProjects>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
