<script setup>
import { defineProps } from 'vue';

defineProps({
    label : String,
    imgURL : String,
    subText: String
});
</script>

<template>
    <div class="flex-1 sm:w-[350px] sm:min-w-[350px] w-full rounded-[20px] shadow-3xl px-10 py-16 hover:border-2 border-coral-red">
        <div class="w-11 h-11 flex justify-center items-center bg-coral-red rounded-full">
            <img :src="imgURL" :alt="label" width="24" height="24">
        </div>
        <h3 class="mt-5 font-palanquin text-3xl leading-normal font-bold">{{ label }}</h3>
        <p class="mt-3 font-montserrat text-lg leading-normal text-slate-gray">{{ subText }}</p>
    </div>
</template>
