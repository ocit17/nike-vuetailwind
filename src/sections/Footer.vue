<script setup>
import { footerLogo } from '../assets/images';
import { copyrightSign } from '../assets/icons';
import { footerLinks, socialMedia } from '../constants';
</script>

<template>
    <footer class="max-container">
        <div class="flex justify-between items-start gap-20 flex-wrap max-lg:flex-col">
            <div class="flex flex-col items-start">
                <a href="">
                    <img :src="footerLogo" width="150" height="46">
                </a>
                <p class="mt-6 text-base leading-7 font-montserrat text-white-400 sm:max-w-sm">Get shoes ready for the new term at your nearest Nike store. Find Your perfect Size In Store. Get Rewards</p>
                <div class="flex items-start gap-5 mt-8">
                    <div v-for="icon in socialMedia" :key="icon.alt" class="flex justify-center items-center w-12 h-12 bg-white rounded-full">
                        <img :src="icon.src" :alt="icon.alt" width="24" height="24">
                    </div>
                </div>
            </div>

            <div class="flex flex-1 justify-between lg:gap-10 gap-20 flex-wrap">
                <div v-for="item in footerLinks" :key="item.title">
                    <h4 class="text-white font-montserrat text-2xl leading-normal font-medium mb-6">{{ item.title }}</h4>
                    <ul v-for="link in item.links" :key="link.name">
                        <li class="mt-3 text-white-400 font-montserrat text-base leading-normal hover:text-slate-gray cursor-pointer">{{ link.name }}</li>
                    </ul>
                </div>
            </div>
        </div>

        <div class="flex justify-between text-white-400 mt-24 max-sm:flex-col max-sm:items-center">
            <div class="flex flex-1 justify-start items-center gap-2 font-montserrat cursor-pointer">
                <img :src="copyrightSign" alt="copy right sign" width="20" height="20" class="rounded-full m-0">
                <p>Copy right. All rights reserved</p>
            </div>
            <p class="font-montserrat cursor-pointer">Term & Conditions</p>
        </div>
    </footer>
</template>