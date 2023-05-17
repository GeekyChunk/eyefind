<template>
        <RouterLink :to="props.link ?? ''" class="flex-grow flex justify-center items-center gap-4 hover:underline hover:text-sky-500">
            <div>
                <component class="h-14 text-sky-500" :is="props.icon" />
            </div>
            <div class="text-lg text-center font-medium">
                <p>{{ props.title1 }}</p>
                <p>{{ props.title2 }}</p>
            </div>
            
        </RouterLink>
</template>

<script setup>
import { defineProps } from 'vue';
import { RouterLink } from 'vue-router';

const props = defineProps({
    title1: { type: String, required: true },
    title2: { type: String, required: true },
    icon: { type: Object, required: true },
    link: { type: String, required: false }
})
</script>