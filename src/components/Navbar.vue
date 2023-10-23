<template>
    <div class="bg-gray-200 text-gray-100 w-full py-3.5 px-6 shadow md:flex justify-between items-center">
            <img src="../assets/logo.png" alt="" class="h-16 w-auto cursor-pointer">
            
        <ul class="md:flex md:items-center md:static absolute w-full top-20 bg-gray-200 left-0 md:w-auto  md:h-full md:max-h-full overflow-hidden duration-700 ease z-10" :class="[open ? 'max-h-96' : 'max-h-0']">
            <li style="white-space: nowrap;" class="md:mx-2 md:my-0 my-8 px-10 md:px-0 lg:mx-4" v-for="item, index in Links" :key="index">
                <a :href="item.link" class="text-xl text-gray-800 w-auto">{{item.name}}</a>
            </li>
        </ul>

        <span class="absolute md:hidden right-6 top-4 cursor-pointer text-5xl text-gray-600">
            <i @click="change" :class="[open ? 'bi bi-x' : 'bi bi-filter-left']"></i>
        </span>
    </div>

</template>

<style scoped>
li a:hover{
    color: #f7bc08;
}
</style>
<script setup>
import {ref} from '@vue/reactivity' 
const open = ref(false)
const change = () => {
    open.value = !open.value
}
const Links = [
    {name : "Inicio", link: "#"},
    {name : "Quienes Somos", link: "#"},
    {name : "Servicios", link: "#"},
    {name : "Experiencia", link: "#"},
    {name : "Contacto", link: "#"},
]
</script>