<script setup>
import MyProjects from '../components/MyProjects.vue'
</script>
<template>
  <div class="content">
    <h1>Projects</h1>
    <MyProjects></MyProjects>
  </div>
</template>

<style scoped>
  h1 {
    font-size: 1.6rem;
    margin: 5rem 0;
    border-bottom: 1px solid var(--secondary-color);
  }

</style>
