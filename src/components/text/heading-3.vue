<script setup lang="ts">
    import { defineProps } from 'vue'

    defineProps({
        text: {
            type: String,
            default: '',
        },
    })
</script>

<template>
    <div class="heading_3">
        <h3 class="heading" v-text="text" />
    </div>
</template>

<style lang="scss">
    @import '@/assets/scss/headings.scss';
</style>
