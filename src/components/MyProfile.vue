<script setup> 
import { RouterLink } from 'vue-router';
import TheButtons from './TheButtons.vue';
</script>

<template>
    <div class="profile-content">
        <div class="text">
            <h1>
                know a little more about<br/>
                my work and studies
            </h1>
            <p>
                I code beautifully simple things, and i love
                what i do.
            </p>
            <div class="buttons">
                <RouterLink to="/projects">
                    <TheButtons title="Projects" :delay="300" class="button"/>
                </RouterLink>
                <RouterLink to="/projects">
                    <TheButtons title="About me" :delay="500" class="button"></TheButtons>
                </RouterLink>
            </div>
        </div>
        <img src="./imgs/Fogueira.gif" alt="">
    </div>
    
</template>

<style scoped>
    .profile-content {
        display: flex;
        justify-content: space-between;
        align-items: center;
        text-align: left;

        margin: 10rem auto;

    }
    .buttons {
        padding: 0;
        font-display: flex;
    }
    .button {
        transition: .5s ease;
        margin: 1rem 0.4rem 1rem 0rem;
    }
    img {
        margin-right: 2rem;
        width: 22rem;
    }
    h1 {
        font-size: 3rem;
        line-height: 3rem;
        color: #fff;
    }
    p {
        margin: 1rem 0;
    }
    @media (max-width: 800px) {
        .profile-content {
            text-align: center;
            flex-direction: column;
            margin: 4rem auto;
        }
        h1 {
            font-size: 2rem;
            line-height: 2.4rem;
        }
        img {
            margin: 1rem auto;
            width: 15rem;
        }
    }
</style>