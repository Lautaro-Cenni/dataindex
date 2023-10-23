<script setup>
import Navbar from "./components/Navbar.vue";
import Slider from "./components/Slider.vue";
import Content from "./components/Content.vue";
import Footer from "./components/Footer.vue";
import Contact from "./components/Contact.vue";
</script>

<template>
  <div class=" h-full">
    <Navbar/>
    <Slider/>
    <Content/>
    <Contact/>
    <Footer/>
  </div>
</template>

<style>
body {
    font-family: 'Comfortaa';
    font-size: 22px;
}
p {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
