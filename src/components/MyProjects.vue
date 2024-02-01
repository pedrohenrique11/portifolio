<script>
import ProjectCard from "./ProjectCard.vue"

import Pomodoros from "./imgs/pomodoros.png"
import Calculadora from "./imgs/calculadora.png"
import BMI from "./imgs/BMI.png"

export default {
    components:{ ProjectCard },
    data() {
        return {
            cards: [
                {title: "Pomodoros", text: "Productivity app based on the Pomodoro technique for focused work intervals.", link: "https://github.com/pedrohenrique11/Pomodoros", img: Pomodoros},
                {title: "BMI Calculator", text: "Body Mass Index (BMI) calculator for quick health and fitness assessment.", link: "https://github.com/pedrohenrique11/BMI-Calculator", img: BMI},
                {title: "Arithmetic calculator", text: "A arithmetic calculator project designed to perform basic mathematical operations.", link: "https://github.com/pedrohenrique11/calculadora_aritmetica/tree/main", img: Calculadora}
            	]
        }
    }
}
</script>

<template>
    <div class="content">
        <ProjectCard v-for="(value, index) in cards" :key="index" :title="value.title" :text="value.text" :link="value.link" :img="value.img"/>
    </div>
</template>

<style scoped>
.content {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

.card {
  flex: 0 1 calc(30% - 20px);
  margin-bottom: 1rem;
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
</style>