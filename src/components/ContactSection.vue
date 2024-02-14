<script setup>
</script>

<template>
    <div class="content">
        <h2>
            Let's make something amazing toghtether!
        </h2>
        <p>
            Start by <span>saying hi</span>
        </p>
        <h3>Pedrohenriqueb.dev@gmail.com</h3>
    </div>
</template>

<style scoped>
    .content{
        display: flex;
        align-items: center;
        flex-direction: column;

        text-align: center;
        margin: 8rem 0 15rem 0;
    }
    h3 {
        margin: 1rem;
        padding: 1rem 1rem;
        border-top: 1px solid var(--secondary-color);
    }
    span {
        color: var(--secondary-color);
    }

    @media (min-width: 800px) {
        h2 {
            font-size: 2.2rem;
        }
        p {
            font-size: 1.4rem;
        }
    }
</style>