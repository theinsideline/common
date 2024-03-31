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
    <div class="paragraph">
        <span v-text="text" />
    </div>
</template>

<style lang="scss">
    @import '@/assets/scss/paragraph.scss';
</style>
