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
        link: {
            type: String,
            default: 'Saiba Mais'
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
        <a :href="link">
            <TheButtons title="View Project" />
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
    border-radius: 3px;
    background-color: var(--primary-dark-color);
    overflow: hidden;

  }
  .card:hover {
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
</style>