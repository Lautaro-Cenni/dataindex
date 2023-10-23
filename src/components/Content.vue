

<template>
    <div>
        <div  id="quienes-somos" class="p-4 md:p-10 mt-10 mb-10" >
            <h2 class="mx-auto w-full text-center text-4xl font-bold mb-3">QUIENES SOMOS</h2>
            <p style="font-family: 'calibri';" class="md:w-10/12 sm:font-bold md:mx-auto flex text-center text-gray-700 md:text-2xl">
                DataIndex, al igual que el índice en un libro, nos guía directamente a las páginas claves que necesitamos explorar para encontrar respuestas y conocimientos ocultos en el océano de datos. Ordenamos y analizamos cada capítulo del libro de tu negocio mediante la designación de indicadores de crecimiento, la extracción e integración de datos de tu empresa, y te contamos su historia con propuestas contundentes y asesorías para que puedas obtener el mejor desenlace.
            </p>
        </div>
        
        <!-- <div style="border-bottom: 2px solid gray;" class="mx-auto w-1/2 mb-7"></div> -->

        <div style="background-color: rgb(255 235 56); color: rgb(45, 47, 51); box-shadow: 10px 6px 25px black;" class="relative pt-8 pb-12 h-full">
            <div class="md:w-11/12 mx-auto flex justify-between">
                <svg style="float: left !important; top: -10px;" fill="rgb(45, 47, 51)" class="hidden md:block relative mk-svg-icon" data-name="mk-moon-quotes-left" data-cacheid="icon-5deb774b62c74" xmlns="http://www.w3.org/2000/svg" width="50px" height="50px" viewBox="0 0 512 512"><path d="M112.5 224c61.856 0 112 50.145 112 112 0 61.856-50.144 112-112 112s-112-50.144-112-112l-.5-16c0-123.712 100.288-224 224-224v64c-42.737 0-82.917 16.643-113.137 46.863-5.817 5.818-11.126 12.008-15.915 18.51 5.719-.9 11.58-1.373 17.552-1.373zm288 0c61.855 0 112 50.145 112 112 0 61.856-50.145 112-112 112s-112-50.144-112-112l-.5-16c0-123.712 100.288-224 224-224v64c-42.737 0-82.917 16.643-113.137 46.863-5.818 5.818-11.127 12.008-15.916 18.51 5.72-.9 11.58-1.373 17.553-1.373z"></path></svg>
                <p style="font-family: 'calibri';" class="mx-auto md:mx-0 text-center text-3xl leading-8 mt-4 max-w-[90%]">
                    Somos más que una empresa global de servicios y soluciones tecnológicas; somos <b>tu aliado estratégico</b>, trabajando a tu lado para <b>superar desafíos</b> y crear un horizonte de <b >oportunidades en tu negocio</b>.
                </p>
                <svg style="float: right !important; top: -10px;" fill="rgb(45, 47, 51)" class="hidden md:block relative mk-svg-icon rotate-180" data-name="mk-moon-quotes-left" data-cacheid="icon-5deb774b62c74" xmlns="http://www.w3.org/2000/svg" width="50px" height="50px" viewBox="0 0 512 512"><path d="M112.5 224c61.856 0 112 50.145 112 112 0 61.856-50.144 112-112 112s-112-50.144-112-112l-.5-16c0-123.712 100.288-224 224-224v64c-42.737 0-82.917 16.643-113.137 46.863-5.817 5.818-11.126 12.008-15.915 18.51 5.719-.9 11.58-1.373 17.552-1.373zm288 0c61.855 0 112 50.145 112 112 0 61.856-50.145 112-112 112s-112-50.144-112-112l-.5-16c0-123.712 100.288-224 224-224v64c-42.737 0-82.917 16.643-113.137 46.863-5.818 5.818-11.127 12.008-15.916 18.51 5.72-.9 11.58-1.373 17.553-1.373z"></path></svg>
            </div>
        </div>
        
        <div id="servicios" class="bg-white">
            <div>
                <p style="font-family: 'comfortaa';" class="w-full text-center text-gray-700 text-4xl font-bold mb-6">
                    Servicios
                </p>
            </div>
            <div id="cards" class="grid lg:grid-cols-3 md:grid-cols-2 grid-cols-1 lg:mx-12 md:mx-10 mx-6 center h-auto">
                <div id="card" v-for="card, index in cards" :key="index" class="rounded-t-xl md:m-6 mx-2 mb-10 h-auto cursor-pointer">
                    <Card 
                    :img = card.img
                    :title = card.title
                    :text =  card.text
                    />
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
#servicios{
    padding-top: 120px;
}
#card {
    transition: all .4s ease;
    transform: scale(1);
}
#card:hover {
    transition: all .4s ease;
    transform: scale(1.05);
    box-shadow: 5px 5px 30px black;
}
</style>

<script setup>
import Card from "./Card.vue";

const cards= [
    {
        img: '../src/assets/extraccion-de-datos.jpg',
        title: 'Extracción de Datos',
        text: 'Agrupamos todos los datos relevantes para tu negocio en un único modelo, sin importar su formato, para que puedas realizar análisis potentes y completos, encontrar correlaciones e incluso pronosticar a futuro utilizando Microsoft Power BI.'
    },

    {
        img:'../src/assets/datawarehouse.jpg',
        title: 'Integración y arquitectura - DataWarehouse',
        text:'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam perferendis reiciendis ex sapiente sed voluptate eaque voluptas numquam! Excepturi porro aspernatur eligendi! Ullam numquam, ipsum nemo molestiae possimus eum sit?'
    },

    {
        img: '../src/assets/automatizacion.jpg',
        title: 'Automatización y mejora de procesos',
        text: 'Te aportamos nuestra experiencia y capacitación en consultoría sobre mejora de procesos de negocios. Implementamos y desarrollamos herramientas digitales para profesionalizar tus procedimientos.'
    },

    {
        img: '../src/assets/kpis-ksis.jpg',
        title: 'Cálculo de KPIs y KSIs',
        text: 'Trabajaremos juntos en la construcción de los mejores indicadores para monitorear el estado y evolución de tu negocio. También contamos con un repositorio de más de 2000 indicadores para utilizar como base de desarrollo.'
    },

    {
        img: '../src/assets/diseño-de-software.jpg',
        title: 'Diseño de Software',
        text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam perferendis reiciendis ex sapiente sed voluptate eaque voluptas numquam! Excepturi porro aspernatur eligendi! Ullam numquam, ipsum nemo molestiae possimus eum sit?'
    },
    
    {
        img: '../src/assets/visualizacion.jpg',
        title: 'Diseño de visualización y Analítica',
        text: 'Lorem ipsum, dolor sit amet consectetur adipisicing elit. Laboriosam perferendis reiciendis ex sapiente sed voluptate eaque voluptas numquam! Excepturi porro aspernatur eligendi! Ullam numquam, ipsum nemo molestiae possimus eum sit?'
    },
]
</script>
