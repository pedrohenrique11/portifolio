<script setup>
import HomeSection from '../components/HomeSection.vue'
import ContactSection from '@/components/ContactSection.vue';
import ProjectCard from '@/components/ProjectCard.vue';
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
    <div data-aos="fade-up" 
    class="profile-content section">
      <ProfileCard class="profile"/>
      <div class="button">
        <RouterLink to="/about">
          <TheButtons title="About-me"/>
        </RouterLink>
      </div>
    </div>
    <h2>Some Projects...</h2>
    <div data-aos="fade-up" 
    class="projects-content section">
        <ProjectCard v-for="(value, index) in cards" 
        :key="index" 
        :title="value.title" 
        :text="value.text" 
        :gitLink="value.gitLink" 
        :projectLink="value.projectLink"
        class="projects-card" />
    </div>
    <div data-aos="fade-up"  class="button">
      <RouterLink to="/projects">
        <TheButtons  title="More Projects"/>
      </RouterLink>
    </div>

      <div data-aos="fade-up" 
      class="contact-content section">
        <ContactSection/>
      </div>
  </main>
</template>

<style scoped>
.profile {
  margin-bottom: 1rem;
}
.button {
  display: flex;
  justify-content: center;

  margin-bottom: 15rem;
}

h2 {
  margin-top: 2rem;
  padding-bottom: 0.4rem;
  text-align: center;

  border-bottom: 1px solid var(--secondary-color);
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
</style>