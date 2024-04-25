<script setup>
import { defineProps } from 'vue';

defineProps([
    'label',
    'iconURL',
    'fullWidth',
    'textColor',
    'animateBtn',
    'borderColor',
    'backgroundColor'
]);
</script>

<template>
    <button
        :class="[
            'flex justify-center items-center gap-1 px-7 py-4 border font-montserrat text-lg leading-none rounded-full group transition-transform', 
            fullWidth ? fullWidth : '',
            textColor ? textColor : 'text-white',
            borderColor ? borderColor : 'border-coral-red',
            backgroundColor ? backgroundColor : 'bg-coral-red',
            animateBtn ? 'hover:-translate-y-1 hover:font-bold' : ''
        ]"
    >

        {{ label }}
        <img v-show="iconURL" :src="iconURL" alt="arrow right icon" :class="['ml-2 rounded-full bg-white w-5 h-5 transition-transform duration-300', animateBtn ? 'group-hover:translate-x-1' : '',]">
    </button>
</template>
