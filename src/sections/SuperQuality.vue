<script setup>
import { shoe8 } from '../assets/images';
import Button from '../components/Button.vue';
</script>

<template>
    <section id="about-us" class="flex justify-between items-center max-lg:flex-col gap-10 max-container">
        <div class="flex flex-1 flex-col">
            <h2 class="font-palanquin capitalize text-4xl lg:max-w-lg font-bold">
                We Provide You <span class="text-coral-red">Super</span> <span class="text-coral-red">Quality</span> Shoes
            </h2>
            <p class="mt-4 lg:max-w-lg info-text">
                Ensuring premium comfort and style, our meticulously crafted footwear
                is designed to elevate your experience, providing you with unmatched
                quality, innovation, and a touch of elegance.
            </p>
            <p class="mt-6 lg:max-w-lg info-text">Our dedication to detail and excellence ensures your satisfaction</p>
            <div class="mt-2">
                <Button label="View details"/>
            </div>
        </div>

        <div>
            <img :src="shoe8" alt="Shoe8" width="570" height="522" class="object-contain">
        </div>
    </section>
</template>