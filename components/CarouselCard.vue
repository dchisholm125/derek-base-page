<script setup lang="ts">
defineProps<{
    imgSrc: any,
    title: string,
    contentText: string,
    btnText: string,
    btnLink: string,
}>()
</script>

<template>
    <div class="card">
        <img :src="imgSrc" class="rounded-top" />
        <div class="card-body">
            <h5 class="card-title">{{ title }}</h5>
            <p class="card-text">{{ contentText }}</p>
            <a :href="btnLink" class="btn btn-primary">{{ btnText }}</a>
        </div>
    </div>
</template>