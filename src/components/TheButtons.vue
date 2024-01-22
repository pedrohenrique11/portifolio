<script>
export default {
    props: {
        title: {
            type: String,
            default: () => "Button"
        }
    }
}
</script>

<template>
        <button>{{ title }}</button>
</template>

<style scoped>
    button{
        padding: 0.8rem 2rem;
        background-color: hsla(160, 100%, 37%, 1);
        border: none;
        border-radius: 5px;
        font-size: 1rem;
        cursor: pointer;
    }
    button:hover {
        background-color: rgb(23, 148, 106);
    }
</style>