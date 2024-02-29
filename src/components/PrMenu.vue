<template>
    <nav>
        <RouterLink v-for="item in menuItems" :to="item.link" class="menu-link">
            <input type="radio" name="" id="" :checked="route.name == item.link">
            <pr-logo :logo="item.logo"></pr-logo>
            <span>{{ item.name }}</span>
        </RouterLink>
    </nav>
</template>

<script setup>
import { RouterLink, useRoute } from 'vue-router'
import PrLogo from './core/PrLogo.vue';

const route = useRoute()

const menuItems = [
    {link: 'skills', name: 'Skills', logo: 'skills'},
    {link: 'education', name: 'Education', logo: 'education'},
    {link: 'experience', name: 'Work Experience', logo: 'experience'},
    {link: 'portfolio', name:'Portfolio', logo: 'portfolio'}
];

</script>

<style scoped>
    .menu-link {
        display: flex;
        padding: 5px;
        align-items: center;
        text-decoration: none;
        color: black;
        font-size: 17px;
        vertical-align: middle;
    }
    .menu-logo {
        display: inline-block;
        height: 40px;
        width: 40px;
        background-color: orange;
        border-radius: 10px;
        margin: 10px;
    }
    .menu-logo:hover {
        text-decoration: underline;
    }

</style>