<script setup>
import { defineProps } from 'vue';

const props = defineProps({
    imgURL : Object,
    bigShoeImg : String,
    changeBigShoeImage: Function
});

const handleClick = () => {
    if (props.bigShoeImg !== props.imgURL.bigShoe) {
        props.changeBigShoeImage(props.imgURL.bigShoe);
    }
}
</script>

<template>
    <div :class="['border-2 rounded-xl cursor-pointer max-sm:flex-1', bigShoeImg === imgURL.bigShoe ? 'border-coral-red' : 'border-transparent']" @click="handleClick">
        <div class="flex justify-center items-center bg-card bg-center bg-cover sm:w-40 sm:h-40 rounded-xl max-sm:p-4">
            <img :src="imgURL.thumbnail" alt="shoe collection" width="127" height="103" class="object-contain">
        </div>
    </div>
</template>
