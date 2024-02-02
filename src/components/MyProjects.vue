<script>
import ProjectCard from "./ProjectCard.vue"

export default {
    components:{ ProjectCard },
    data() {
        return {
            cards: [
                {title: "Pomodoros", text: "Productivity app based on the Pomodoro technique for focused work intervals.", projectLink:"https://pedrohenrique11.github.io/Pomodoros/", gitLink: "https://github.com/pedrohenrique11/Pomodoros"},
                {title: "BMI Calculator", text: "A Body Mass Index (BMI) calculator for quick health and fitness assessment.", projectLink:"https://pedrohenrique11.github.io/BMI-Calculator/", gitLink: "https://github.com/pedrohenrique11/BMI-Calculator"},
                {title: "Arithmetic calculator", text: "A arithmetic calculator project designed to perform basic mathematical operations.", projectLink:"https://calculadora-aritmetica-flax.vercel.app/", gitLink: "https://github.com/pedrohenrique11/calculadora_aritmetica/tree/main"},
                {title: "Em Construção... 👨🏻‍💻", text: "Come back again later and maybe I'll have something new to show you...", projectLink:"", gitLink: ""},
                {title: "Em Construção... 👨🏻‍💻", text: "Come back again later and maybe I'll have something new to show you...", projectLink:"", gitLink: ""},
                {title: "Em Construção... 👨🏻‍💻", text: "Come back again later and maybe I'll have something new to show you...", projectLink:"", gitLink: ""}

            	],
              loaded: false,
        };
    },
    mounted() {
    setTimeout(() => {
      this.loaded = true;
    }, 100);
  }
}

</script>

<template>
    <div class="content">
        <ProjectCard v-for="(value, index) in cards" 
        :key="index" 
        :title="value.title" 
        :text="value.text" 
        :gitLink="value.gitLink" 
        :projectLink="value.projectLink"
        class="card" 
        :class="{'slide-up':loaded}"
        :style="{'transition-delay': `${index * 0.1}s`}"/>
    </div>
</template>

<style scoped>
.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 40px;
}

.card {
  flex: 0 1 calc(34% - 20px);
  margin-bottom: 1rem;
  transition: transform 0.5s ease, border 1s ease;
}

@media (max-width: 1100px) {
    .card {
      flex-basis: calc(50% - 20px);
    }
}
@media (max-width: 800px) {
  .card {
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