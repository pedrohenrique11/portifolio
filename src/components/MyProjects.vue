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
                {title: "Arithmetic calculator", text: "Simple calculator for basic arithmetic operations.", link: "https://github.com/pedrohenrique11/calculadora_aritmetica/tree/main", img: Calculadora},
                {title: "Guessing game", text: "Fun game to guess a random number within a specified range.", link: "https://github.com/pedrohenrique11/guessing-game", img:"", }
            ]
        }
    }
}
console.log(BMI)
</script>

<template>
    <div class="content">
        <ProjectCard v-for="(value, index) in cards" :key="index" :title="value.title" :text="value.text" :link="value.link" :img="value.img"/>
    </div>
</template>

<style >
</style>