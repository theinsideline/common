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
        <span v-if="text" v-text="text" />
        <span v-else><slot /></span>
    </div>
</template>

<style lang="scss">
    @import '@/assets/scss/paragraph.scss';
</style>
