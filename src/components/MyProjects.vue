<script>
import ProjectCard from "./ProjectCard.vue"

export default {
    components:{ ProjectCard },
    data() {
        return {
            cards: [
                {title: "Pomodoros", text: "Productivity app based on the Pomodoro technique for focused work intervals.", link: "https://github.com/pedrohenrique11/Pomodoros"},
                {title: "BMI Calculator", text: "A Body Mass Index (BMI) calculator for quick health and fitness assessment.", link: "https://github.com/pedrohenrique11/BMI-Calculator"},
                {title: "Arithmetic calculator", text: "A arithmetic calculator project designed to perform basic mathematical operations.", link: "https://github.com/pedrohenrique11/calculadora_aritmetica/tree/main"},
                {title: "Em Construção", text: "", link: ""},
                {title: "Em Construção", text: "", link: ""},
                {title: "Em Construção", text: "", link: ""}

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
        :link="value.link" 
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
  flex: 0 1 calc(30% - 20px);
  margin-bottom: 1rem;
  transition: transform .5s ease;
}

@media (max-width: 1100px) {
    .card {
      flex-basis: calc(50% - 20px);
    }
}
@media (max-width: 600px) {
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