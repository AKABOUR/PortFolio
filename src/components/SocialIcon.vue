<script setup>
    const props = defineProps({
        img: String,
        link: String,
        alt: String
    })
    // Import dynamique
const imageUrl = new URL(`/src/assets/${props.img}.png`, import.meta.url).href
</script>

<template>
    <a :href="props.link" target="_blank">
        <img class="social-img" :src="imageUrl" :alt="props.alt" width="32px"/>
    </a>
</template>

<style scoped>
    .social-img {
        margin-right: 10px;
        filter: opacity(0.8);
    }
</style>