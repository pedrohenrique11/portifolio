<script setup>
import ProjectCard from '@/components/ProjectCard.vue';
import HomeSection from '../components/HomeSection.vue'
import ProfileCard from '../components/ProfileCard.vue'
import TheButtons from '@/components/TheButtons.vue';
import { RouterLink } from 'vue-router';

const cards = [
    {title: "Pomodoros", text: "Productivity app based on the Pomodoro technique for focused work intervals.", projectLink:"https://pedrohenrique11.github.io/Pomodoros/", gitLink: "https://github.com/pedrohenrique11/Pomodoros"},
    {title: "BMI Calculator", text: "A Body Mass Index (BMI) calculator for quick health and fitness assessment.", projectLink:"https://pedrohenrique11.github.io/BMI-Calculator/", gitLink: "https://github.com/pedrohenrique11/BMI-Calculator"},
   
];

</script>

<template>
  <main>
    <HomeSection />
    <div class="profile-content">
      <ProfileCard class="profile"/>
      <RouterLink to="/about">
        <TheButtons class="button" title="About-me"/>
      </RouterLink>
    </div>
    <h2>Some projects...</h2>
    <div class="projects-content">
        <ProjectCard v-for="(value, index) in cards" 
        :key="index" 
        :title="value.title" 
        :text="value.text" 
        :gitLink="value.gitLink" 
        :projectLink="value.projectLink"
        class="projects-card" />
    </div>
      <RouterLink to="/projects">
        <TheButtons class="button p" title="Projects"/>
      </RouterLink>
  </main>
</template>

<style scoped>

.profile {
  margin-bottom: 1rem;
}
.button {
  margin-bottom: 12rem;
}

h2 {
  margin-top: 2rem;
  text-align: center;
}
.projects-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 40px;
}

.projects-card {
  flex: 0 1 calc(50% - 20px);
  margin-bottom: 1rem;
  transition: transform 0.5s ease, border 1s ease;
}

@media (max-width: 800px) {
  .projects-card {
    flex-basis: calc(100%);
  }
}
@media (min-width: 800px) {
  .p {
    margin-left: 10px;
  }
}
</style>