<script>
import TheButtons from './TheButtons.vue';

    export default {
    props: {
        title: {
          type: String,
          required: true
        },
        text: {
          type: String,
          required: true
        },
        projectLink: {
          type: String,
        },
        gitLink: {
          type: String,
        }
    },
    components: { TheButtons }
}
</script>
<template>
    <div class="card">
      <div class="card-content">
        <h2 class="card-title">{{ title }}</h2>
        <p class="card-text">{{ text }}</p>
        <a :href="projectLink">
            <TheButtons title="Live demo" class="button"/>
        </a>
        <a :href="gitLink">
            <TheButtons title="Repositorie" class="button secondary-button"/>
        </a>
      </div>
    </div>
</template>
  
<style scoped>
  .card-container {
    perspective: 1000px;
  }
  .card {
    padding: 0;
    margin: 0 auto;
    border-radius: 3px;
    background-color: var(--primary-dark-color);
    border: 1px solid var(--primary-dark-color);
    overflow: hidden;
    	
    transition: 2s;
  }
  .card:hover {
    border: 1px solid var(--secondary-color);
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  }
  .card-content {
    padding: 20px;
  }
  .card-title {
    font-size: 1.5rem;
    margin-bottom: 10px;
  }
  .card-text {
    margin-bottom: 15px;
    color: #666;
  }
  a {
    text-align: center;
  }
  .secondary-button {
    margin-left: 1rem;
    color: #fff;
    background-color: var(--primary-dark-color);
    border: 1px solid var(--secondary-color);
  }
</style>