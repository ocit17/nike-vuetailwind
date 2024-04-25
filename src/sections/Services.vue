<script setup>
import ServiceCard from '../components/ServiceCard.vue';
import { services } from '../constants';
</script>

<template>
    <section class="max-container flex justify-center flex-wrap gap-9">
        <ServiceCard v-for="(item, index) in services" :key="index" :label="item.label" :imgURL="item.imgURL" :subText="item.subtext"/>
    </section>
</template>