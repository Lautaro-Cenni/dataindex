<template>
    <div style="background-color: rgb(20, 18, 0);" id="test" class="p-10 text-gray-200 h-[550px]">
        <div class="w-full">
            <div style="border-bottom: 1px solid rgb(110, 108, 108);" class="flex relative top-0 left-0 mt-7 mb-6"></div>
                <div style="width: 300px;">
                    <img  src="../assets/logo horizontal blanco.png" alt="">
                </div>
          </div>
        
        <div class="ml-7 mt-9 w-full grid lg:grid-cols-3 grid-cols-1">
            <div class="">
                <h1 class="text-bold text-2xl">CONTACTO</h1>
                <h2 class="text-xl">TEL: +54 9 1156367714</h2>
                <h2 class="text-xl ">MAIL: wearedataindex@gmail.com</h2>
            </div>
            <div>texto2</div>
            <div>texto3</div>
        </div>
        <div class="relative bottom-0 left-0 w-full">
            <div class="mx-auto w-min flex">
                <div v-for="icon,index in icons" :key="index" class="red-social-icono-contenedor">
                    <a :href="icon.link">
                        <i style="font-size: 20px;" :class="icon.icon"></i>
                    </a>
                </div>
            </div>
        </div>
        <div class="box"></div>
    </div>
</template>

<style scoped>
/* #test{ animation: fade-in 2s forwards; 
    animation-iteration-count: infinite;}
@keyframes fade-in {
  0% { background-color: rgb(41, 40, 40); }
  50% { background-color: rgb(37, 36, 36); }
  100% { background-color: rgb(41, 40, 40); }
} */
h2 {
    margin-top: 8px;
}
i {
    display: inline-block;
    width: 100%;
    text-align:center;
}
.red-social-icono-contenedor{
    background-color: transparent;
    width: 50px;
    height: 50px;
    line-height: 45px;
    border: 1px solid hsla(0,0%,100%,.1);
    border-radius: 50px;    
    margin-right: 15px;
    z-index: 10;
    transition: all 2s, color .4s;
    box-shadow: inset 0 0 0 150px rgb(20, 18, 0);
    
}
.red-social-icono-contenedor:hover {
    background-color: white;
    transition: all .4s, color .6s;
    color: black;
    box-shadow: inset 0 0 0 0 rgb(20, 18, 0);
}
</style>

<script setup>
const icons = [
    {
        icon : "bi bi-linkedin",
        link : "https://www.linkedin.com/company/wearedataindex/about/?viewAsMember=true"
    },
    {
        icon : "bi bi-linkedin",
        link : "https://www.linkedin.com/company/wearedataindex/about/?viewAsMember=true"
    },
    {
        icon : "bi bi-linkedin",
        link : "https://www.linkedin.com/company/wearedataindex/about/?viewAsMember=true"
    },
]
</script>