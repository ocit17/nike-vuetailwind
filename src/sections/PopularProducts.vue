<script setup>
import { products } from '../constants';
import PopularProductCard from '../components/PopularProductCard.vue';
</script>

<template>
    <section id="products" class="max-container max-sm:mt-12">
        <div class="flex flex-col justify-start gap-5">
            <h2 class="text-4xl font-palanquin font-bold">
                Our<span class="text-coral-red"> Popular</span> Products
            </h2>
            <p class="lg:max-w-lg mt-2 font-montserrat text-slate-gray text-justify">Experience top-notch quality and style with our sought-after selections. Discover a world of comfort, design, and value</p>
        </div>

        <div class="mt-16 grid lg:grid-cols-4 md:grid-cols-3 sm:grid-cols-2 grid-cols-1 sm:gap-4 gap-14">
            <PopularProductCard v-for="item in products" :key="item.name" :name="item.name" :price="item.price" :imgURL="item.imgURL"/>
        </div>
    </section>
</template>