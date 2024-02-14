<script setup>
import ProjectCard from "./ProjectCard.vue";
import { ref, onMounted } from "vue"

const cards = [
    {title: "Pomodoros", text: "Productivity app based on the Pomodoro technique for focused work intervals.", projectLink:"https://pedrohenrique11.github.io/Pomodoros/", gitLink: "https://github.com/pedrohenrique11/Pomodoros"},
    {title: "BMI Calculator", text: "A Body Mass Index (BMI) calculator for quick health and fitness assessment.", projectLink:"https://pedrohenrique11.github.io/BMI-Calculator/", gitLink: "https://github.com/pedrohenrique11/BMI-Calculator"},
    {title: "Arithmetic calculator", text: "An arithmetic calculator project designed to perform basic mathematical operations.", projectLink:"https://calculadora-aritmetica-flax.vercel.app/", gitLink: "https://github.com/pedrohenrique11/calculadora_aritmetica/tree/main"},
    {title: "Under Construction... 👨🏻‍💻", text: "Come back again later and maybe I'll have something new to show you...", projectLink:"", gitLink: ""},
    {title: "Under Construction... 👨🏻‍💻", text: "Come back again later and maybe I'll have something new to show you...", projectLink:"", gitLink: ""},
    {title: "Under Construction... 👨🏻‍💻", text: "Come back again later and maybe I'll have something new to show you...", projectLink:"", gitLink: ""}
];

const loaded = ref(false);

onMounted(() => {
    setTimeout(() => {
        loaded.value = true;
    }, 100);
});
</script>

<template>
    <div class="projects-content">
        <ProjectCard v-for="(value, index) in cards" 
        :key="index" 
        :title="value.title" 
        :text="value.text" 
        :gitLink="value.gitLink" 
        :projectLink="value.projectLink"
        class="projects-card" 
        :class="{'slide-up':loaded}"
        />
    </div>
</template>

<style scoped>
.projects-content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 40px;
}

.projects-card {
  flex: 0 1 calc(34% - 20px);
  margin-bottom: 1rem;
  transition: transform 0.5s ease, border 1s ease;
}

@media (max-width: 1100px) {
    .projects-card {
      flex-basis: calc(50% - 20px);
    }
}
@media (max-width: 800px) {
  .projects-card {
    flex-basis: calc(100% - 20px);
  }
}
.below-menu {
  z-index: 1;
}
.slide-up {
  z-index: 1;
  transform: translateY(-40px);
}
</style>