<template>
    <section class="page-content">
        <slot />
    </section>
</template>

<script setup>

const props = defineProps(['title', 'logo'])

</script>

<style scoped>
    .page-header {
        display: flex;
        justify-content: space-between;
        padding: 10px;
        margin-top: 30px;
    }
    .page-header h3 {
        display: flex;
        align-items: center;
        font-size: 25px;
        color: black;
        font-weight: normal;
    }
    .contact-button {
        display: flex;
        align-items: center;
        background: #FFFFFF;
        box-shadow: 10px 15px 10px rgba(183, 183, 183, 0.3);
        border-radius: 10px;
        padding: 10px;
        text-decoration: none;
        color: black;
        font-weight: 300;
    }
    .page-content {
        padding: 20px;
    }
</style>