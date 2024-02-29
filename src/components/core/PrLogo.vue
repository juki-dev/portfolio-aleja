<template>
    <div :style="{backgroundColor:logo.color}" class="logo">
    </div>
</template>

<script setup>

const props = defineProps(['logo'])

const logos = {
    skills: {
        image: 'skills',
        color: 'orange',
    },
    education: {
        image: 'education',
        color: 'green',
    },
    experience: {
        image: 'experience',
        color: 'blue',
    },
    portfolio: {
        image: 'portfolio',
        color: 'blueviolet',
    }
}

const logo = logos[props.logo]


</script>

<style scoped>
    .logo {
        display: inline-block;
        height: 40px;
        width: 40px;
        background-color: orange;
        border-radius: 10px;
        margin: 10px;
    }

</style>