<script>
export default {
    props: {
        title: {
            type: String,
            default: () => "Button"
        },
        delay: {
            type: Number,
            default: 200
        }
    },
    data() {
            return {
                loaded: false,
            }
        },
        mounted() {
            setTimeout (() => {
                this.loaded = true
            }, this.delay) 
        }
}
</script>

<template>
        <button :class="{'slide-up': loaded}">{{ title }}</button>
</template>

<style scoped>
    button{
        padding: 0.6rem 1.8rem;
        margin-top: 2rem;

        background-color: var(--secondary-color);
        color: #000;

        border: none;
        border-radius: 3px;

        font-size: 1rem;
        font-weight: 500;

        transition: .3s;
        cursor: pointer;
    }
    button:hover {
        padding: 0.6rem 2.2rem;
        background-color: #35a8ce;
    }
    .slide-up {
        transform: translateY(-20px);
    }
</style>