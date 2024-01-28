<script>

</script>

<template>
    <div class="content">
        <div class="text">
            <h1>
                Pedro Henrique
            </h1>
            <p>
                Front-End Developer
            </p>
        </div>
        <img src="../components/imgs/Illustration.svg" alt="">
    </div>
    
</template>

<style scoped>
    .content {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 2rem 0 0 0;
    }
    .text {
        position: absolute;
    }
    img {
        margin-left: 50%;
        width: 20rem;
    }
    h1 {
        font-size: 3rem;
        line-height: 3rem;
        color: #fff;
    }
    @media (max-width: 700px) {
        img {
            width: 14rem;
        }
    }
</style>