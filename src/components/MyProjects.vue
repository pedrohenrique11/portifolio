<script>
import ProjectCard from "./ProjectCard.vue"

export default {
    components:{ ProjectCard },
    data() {
        return {
            cards: [
                {title: "Pomodoros", text: "Productivity app based on the Pomodoro technique for focused work intervals.", link: "https://github.com/pedrohenrique11/Pomodoros", img: "../components/imgs/pomodoros.png"},
                {title: "BMI Calculator", text: "Body Mass Index (BMI) calculator for quick health and fitness assessment.", link: "https://github.com/pedrohenrique11/BMI-Calculator", img: "../components/imgs/BMI.png"},
                {title: "Arithmetic calculator", text: "Simple calculator for basic arithmetic operations.", link: "https://github.com/pedrohenrique11/calculadora_aritmetica/tree/main", img: "../components/imgs/calculadora.png"},
                {title: "Guessing game", text: "Fun game to guess a random number within a specified range.", link: "https://github.com/pedrohenrique11/guessing-game", img: "../components/imgs/BMI.png"}
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

<style >
</style>