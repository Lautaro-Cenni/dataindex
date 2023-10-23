<template>
    <div class="lg:h-[480px] md:h-[440px] relative rounded-t-xl bg-white">
        <div>
            <img class=" md:h-[140px] relative w-full rounded-t-xl object-cover top-0" :src="img"  alt="">
        </div>
        <div style="border: 2px solid #cfd1ca; border-top: none;" class="p-8 md:h-[300px] lg:h-[340px]">
            <div class="w-full text-center text-gray-700 text-xl font-bold mb-4">
                {{ title }}
            </div>
            <div class="text-gray-500 text-sm font-bold">{{ text }}
            </div>
        </div>
    </div>
</template>

<script setup>
const props = defineProps(
    {
    img:String,
    title:String,
    text:String 
    })
</script>