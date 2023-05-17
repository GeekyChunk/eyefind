<template>
    <div class="">
        <div class="bg-sky-600 px-16 py-4 border-b-[1rem] border-amber-400">
            <div class="container mx-auto">
                <div class="flex flex-wrap items-center justify-center lg:justify-between">
                    <img class="w-auto h-16" src="/main.png" alt="">
                    
                    <div class="flex items-center">
                        <img class="w-auto h-12" src="/cloud.png" alt="">
                        <div class="flex flex-col gap-2 text-white font-semibold">
                            <h3 class="text-xl">Winewood Hills</h3>
                            <h3 class="text-2xl">Sun</h3>
                        </div>
                    </div>
                </div>
    
                <div class="flex justify-center lg:justify-between items-center pt-4">
                    <div class="w-full lg:px-8">
                        <div class="w-full relative flex items-center">
                            <MagnifyingGlassIcon class="absolute w-7 ml-3 text-sky-400 focus:text-sky-600" />
                            <input class="w-full input input-bordered ps-12" placeholder="Search EyeFind" type="text">
                        </div>
                    </div>
                    <div class="w-full lg:max-w-[14rem]">
                        <button class="btn btn-primary py-3 h-auto w-full text-xl">Random</button>
                    </div>
                </div>
            </div>
        </div>
        <div class="bg-zinc-200 border-b-4 border-cyan-500">
            <div class="container mx-auto">
                <div class="flex flex-wrap justify-center py-4 gap-4 gap-y-8">
                    <template v-for="service, i in services">
                        <ServiceItem :title1="service.title1" :title2="service.title2" :icon="service.icon" />
                        <div v-if="i != (services.length-1)" className="divider divider-vertical lg:divider-horizontal before:bg-sky-300 after:bg-sky-300"></div> 
                    </template>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import { MagnifyingGlassIcon, CurrencyDollarIcon, ShoppingBagIcon } from '@heroicons/vue/24/solid';
import { DevicePhoneMobileIcon } from '@heroicons/vue/24/outline';
import FoodIcon from "../icons/footIcon.vue"
import ServiceItem from './ServiceItem.vue';
import TravelIcon from '../icons/travelIcon.vue';

const services = [
    { title1: "MEDIA AND", title2: "ENTERTAINMENT", icon: DevicePhoneMobileIcon },
    { title1: "FOOT AND", title2: "DRINK", icon: FoodIcon },
    { title1: "MONEY AND", title2: "SERVICES", icon: CurrencyDollarIcon },
    { title1: "TRAVEL AND", title2: "TRANSPORT", icon: TravelIcon },
    { title1: "FASHION AND", title2: "HEALTH", icon: ShoppingBagIcon },
]

</script>