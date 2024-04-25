<script setup>
import { reviews } from '../constants';
import ReviewCard from '../components/ReviewCard.vue';
</script>

<template>
    <section class="max-container">
        <h3 class="font-palanquin text-center text-4xl font-bold">What Our <span class="text-coral-red">Customers</span> Says ?</h3>
        <p class="m-auto mt-4 max-w-lg text-center info-text">Hear genuine stories from our satisfied customers about theirexceptional experiences with us.</p>
        <div class="mt-24 flex flex-1 justify-evenly items-center max-lg:flex-col gap-14">
            <ReviewCard v-for="(item, index) in reviews" :key="index"
            :rating="item.rating"
            :imgURL="item.imgURL"
            :feedback="item.feedback"
            :customerName="item.customerName"
            />
        </div>
    </section>
</template>