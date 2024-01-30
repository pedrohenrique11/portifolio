<script>

</script>

<template>
    <div class="button-container">
        <button>
            <svg xmlns="http://www.w3.org/2000/svg" height="38" viewBox="0 -960 960 960" width="38"><path d="M120-240v-80h720v80H120Zm0-200v-80h720v80H120Zm0-200v-80h720v80H120Z"/></svg>
        </button>
    </div>
</template>

<style scoped>
    .button-container {
        position: fixed;
        bottom: 2rem;
        right: 2rem;
    }
    button {
        display: flex;
        justify-content: center;
        align-content: center;
        padding: 0.5rem 0.6rem;

        background: rgba(0, 189, 126, 0.81);
        border-radius: 16px;
        box-shadow: 0 4px 30px rgba(0, 0, 0, 0.1);
        backdrop-filter: blur(0.9px);
        -webkit-backdrop-filter: blur(0.9px);

        border-radius: 5px;
        border: none;
        cursor: pointer;

        transition: 0.5s;
    }
    button:hover {
        background: rgba(0, 189, 126, 1);
    }

    @media (min-width: 700px) {
        .button-container {
            display: none;
        }
    }
</style>