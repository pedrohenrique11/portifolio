<script setup> 
import { RouterLink } from 'vue-router';
import TheButtons from './TheButtons.vue';

</script>

<template>
    <div class="content">
        <div class="text">
            <h1>
                know a little more about
                my work and studies
            </h1>
            <p>
                I code beautifully simple things, and i love
                what i do.
            </p>
            <div class="buttons">
                <RouterLink to="/projects">
                    <TheButtons title="Projects"/>
                </RouterLink>
                <RouterLink to="/projects">
                    <TheButtons title="About me"/>
                </RouterLink>
            </div>
        </div>
    </div>
    
</template>

<style scoped>
    .content {
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: center;

        margin: 5rem auto;
        padding: 2rem 0 0 0;

        max-width: 800px;
    }
    .buttons {
        padding: 0;
        font-display: flex;
    }
    img {
        width: 20rem;
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
        .content {
            flex-direction: column;
        }
        h1 {
            font-size: 2rem;
            line-height: 2.4rem;
        }
        img {
            margin-top: 1rem;
            width: 17rem;
        }
    }
</style>