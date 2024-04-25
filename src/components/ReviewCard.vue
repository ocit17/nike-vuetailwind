<script setup>
import { defineProps } from 'vue';
import { star } from '../assets/icons';

defineProps({
    rating: Number,
    imgURL : String,
    feedback: String,
    customerName : String,
});
</script>

<template>
    <div class="flex justify-center items-center flex-col">
        <img :src="imgURL" alt="customer" class="rounded-full object-cover w-[120px] h-[120px] hover:border-2 hover:shadow-3xl border-coral-red">
        <p class="mt-6 flex justify-center items-center gap-2.5">{{ feedback }}</p>
        <div>
            <img :src="star" alt="rating star" width="24" height="24" class="object-contain m-0">
            <p class="text-xl font-montserrat text-slate-gray">{{ rating }}</p>
        </div>
        <h3 class="mt-1 font-palanquin text-3xl text-center font-bold">{{ customerName }}</h3>
    </div>
</template>