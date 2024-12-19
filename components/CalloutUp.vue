<script setup lang="ts">
defineProps<{
    text: string,
}>()
</script>

<template>
    <h6 class="d-flex text-nowrap callout-font">
        <img src="~/assets/img/arrow-90deg-up.svg" height="40" width="40" />
        <span 
            class="align-self-end ms-2 fw-medium fs-5" 
            style="transform: translateY(8px)">
                {{ text }}
        </span>
    </h6>
</template>

<style scoped>

.callout-font{
    font-family: 'Courier New', Courier, monospace;
}

</style>