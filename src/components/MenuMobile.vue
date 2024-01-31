<script setup>
import { RouterLink } from 'vue-router';
import { ref } from 'vue';
import ButtonMenu from './ButtonMenu.vue';

const isActive = ref(false);

const toggle = () => {
     isActive.value = !isActive.value;
}

</script>

<template>
    <div ref="menu" id="menu" :class="{'menu': true, 'active': isActive}">
            <li :onClick="toggle">
                <RouterLink to="/">Home</RouterLink>
            </li>
            <li :onClick="toggle">
                <RouterLink to="/projects">Projects</RouterLink>
            </li>
            <ButtonMenu :onClick="toggle"/>
    </div>
    <ButtonMenu :onClick="toggle"/>
</template>

<style scoped>
    .menu{
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        position: fixed;
        width: 0;
        height: 100%;
        top: 0;
        right: 0px;
        box-shadow: 0 5px 10px rgba(0, 0, 0, .5);
        background-color: rgba(0, 0, 0, .8);
        z-index: 100;
        transition: .5s;
        visibility: hidden;
        overflow-x: hidden;
    }
    .active {
        width: 80vw;
        visibility: visible;
        overflow-x: auto;
    }
    li {
        list-style: none;
        font-size: 2rem;
        font-weight: 400;
        margin: 0.4rem;
    }
</style>