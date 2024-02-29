<template>
    <div>
        <h5 class="title">Skills</h5>
        <div>
            <pr-card v-for="skill in skills">
                <span :logo="skill.logo"></span>
                <span>{{ skill.title }}</span>
            </pr-card>
        </div>
    </div>
</template>

<script setup>

import PrCard from './core/PrCard.vue';

const skills = [
    {logo: 'tt', title: 'Creative Writing'},
    {logo: 'tt', title: 'Figma'},
    {logo: 'tt', title: 'Teamwork'},
    {logo: 'tt', title: 'Customer Journey'},
]

</script>

<style scoped>
    .title {
        margin: 20px 10px;
        font-size: 16px;
        font-weight: 500;
    }
</style>
