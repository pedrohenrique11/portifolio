<script>

</script>

<template>
    <div class="content">
        <a href="https://github.com/pedrohenrique11/Pomodoros">
            <div class="project-container">
                <img src="../components/imgs/pomodoros.png" alt="">
                <h4>Pomodoros</h4>
                <p>Productivity app based on the Pomodoro technique for focused work intervals.</p>
            </div>
        </a>
        <a href="https://github.com/pedrohenrique11/BMI-Calculator">
            <div class="project-container">
                <img src="../components/imgs/BMI.png" alt="">
                <h4>BMI Calculator</h4>
                <p>Body Mass Index (BMI) calculator for quick health and fitness assessment.</p>
            </div>
        </a>
        <a href="https://github.com/pedrohenrique11/calculadora_aritmetica/tree/main">
            <div class="project-container">
                <img src="../components/imgs/calculadora.png" alt="">
                <h4>Arithmetic calculator</h4>
                <p>Simple calculator for basic arithmetic operations.</p>
            </div>
        </a>
        <a href="">
            <div class="project-container">
                <img src="" alt="">
                <h4>Guessing game</h4>
                <p>Fun game to guess a random number within a specified range.</p>
            </div>
        </a>
    </div>
</template>

<style scoped>
.content {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 2rem;
}
.project-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;

    border-radius: 5px;
    padding: 2rem 1rem;
    background-color: #2D2E32;
}
.project-containe:hover {
    box-shadow: 10px 10px 15px -3px rgba(0,0,0,0.1);
}
h4 {
    font-size: 1.2rem;
    margin-top: 0.6rem;
}
img {
    width: 16rem;
    height: 10rem;
    border-radius: 5px;
}
a {
    color: #fff;
}
a:hover {
    color: hsla(160, 100%, 37%, 1);
}
@media (max-width: 700px){
    .content {
        grid-template-columns: repeat(1, 1fr);
    }
    img {
        width: 25rem;
        height: 15.2rem;
    }
}
</style>