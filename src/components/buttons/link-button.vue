<script setup lang="ts">
    import { defineProps } from 'vue'

    defineProps({
        text: {
            type: String,
            default: '',
        },
        link: {
            type: String,
            default: '',
        },
        color: {
            type: String,
            default: '#161616',
        },
    })
</script>

<template>
    <a class="link-button" :href="link" :style="`background: ${color};`">{{ text }} <i>--></i></a>
</template>

<style lang="scss">
    @import '@/assets/scss/fonts.scss';
    @import '@/assets/scss/breakpoints.scss';

    .link-button {
        cursor: pointer;
        text-decoration: none;
        color: white;
        text-align: center;
        width: 100%;
        max-width: 350px;
        padding: 12px;
        border-radius: 30px;
        font-family: Inter;
        font-size: $link_button_font_size;

        &:hover {
            background: #747474;
            transition: all 0.3s ease-in-out;

            i {
                animation: MoveLeftRight 1s linear infinite;
                position: relative;
                right: 0;
            }

            @keyframes MoveLeftRight {
                0%,
                100% {
                    right: 0;
                }
                50% {
                    right: -3px;
                }
            }
        }
    }

    @include mobile {
        .link-button {
            font-size: $link_button_font_size_mobile;
        }
    }

    @include tablet {
        .link-button {
            font-size: $link_button_font_size_mobile;
        }
    }

    @include laptop {
        .link-button {
            font-size: $link_button_font_size_mobile;
        }
    }

    @include desktop {
        .link-button {
            font-size: $link_button_font_size_mobile;
        }
    }
</style>
