<template>
    <div class="slider relative h-[420px]">
        <ul style="background-color: rgba(0,0,0,0.5);" class="h-full">
            <li v-for="text, index in texts" :key="index" :class="[id == index ? '' : 'hidden']" class="relative h-full">
                <div class="absolute top-0 left-0 w-full h-full flex">
                    <h2 class="text-4xl font-bold text-white w-full my-auto text-center">{{text.title}}</h2>
                </div>
            </li>
        </ul>
        <div class="absolute flex h-full w-full top-0 left-0 opacity-30 hover:opacity-100 duration-700 ease">
            <div class="md:my-auto w-full flex justify-between md:px-5 opacity-0 md:opacity-100">
                <button @click="prev" class="w-1/2 md:w-auto md:p-3 border-solid border-4 border-white rounded-full ">
                    <svg style="stroke:white;stroke-width:4px" fill="white" xmlns="http://www.w3.org/2000/svg" width="24" height="24"><path d="M15.293 3.293 6.586 12l8.707 8.707 1.414-1.414L9.414 12l7.293-7.293-1.414-1.414z"/>
                    </svg>
                </button>
                <button @click="next" class="w-1/2 md:w-auto md:p-3 border-solid border-4 border-white rounded-full ">
                    <svg style="stroke:white;stroke-width:4px" fill="white" xmlns="http://www.w3.org/2000/svg" width="24" height="24"><path d="M7.293 4.707 14.586 12l-7.293 7.293 1.414 1.414L17.414 12 8.707 3.293 7.293 4.707z"/>
                    </svg>
                </button>
            </div>
        </div>
        <div class="flex absolute bottom-0 left-0 w-full h-14">
            <div class="my-auto mx-auto flex">
                <div v-for="item,index in texts" :key="index" class="mx-2 cursor-pointer">
                    <div v-if="index!=id" @click="change(index)">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                            <circle cx="12" cy="12" r="7" fill="transparent" stroke="white" stroke-width="3" />
                        </svg>
                    </div>
                    <div v-else clase="cursor-pointer">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                            <circle cx="12" cy="12" r="10" fill="transparent" stroke="white" stroke-width="4" />
                            <circle cx="12" cy="12" r="3" fill="white" stroke="white" stroke-width="2" />
                        </svg>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
.slider {
    background-image: url('../assets/banner.jpg');
}
</style>

<script setup>
    import {ref} from '@vue/reactivity' 
    const id = ref(0)
    const texts = [
        {
            title: 'Data Engineer – ETL y Big Data'
        },
        {
            title: 'Data Analytics - Business Intelligence'
        },
        {
            title: 'placeHolder1 - xdxdxdxdxd'
        }
    ]
    const next = () => {
        if (id.value == texts.length-1) {
            id.value = 0
        }
        else {
            id.value++
        }
    }
    const prev = () => {
        if (id.value == 0) {
            id.value = texts.length-1
        }
        else {
            id.value--
        }
    }

    const change = (value) => {
        console.log(value)
        id.value = value
        console.log(id)
    }
</script>