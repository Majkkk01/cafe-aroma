<script setup>
import Navbar from "./components/Navbar.vue"
import Home from "./components/sections/Home.vue"
import MenuCafe from "./components/sections/Menu.vue"
import About from "./components/sections/About.vue"
import Contact from "./components/sections/Contact.vue"
import Footrik from "./components/Footer.vue"

</script>

<template>
   <div id="app">
    <Navbar />  <!-- Zobrazení Navbaru -->
    <Home/>
    <div class="divider"></div>
    <MenuCafe/>
    <div class="divider"></div>
    <About/>
    <div class="divider"></div>
    <Contact/>
    <Footrik/>
  </div>
</template>

<style scoped>

html {
  scroll-behavior: smooth;
}

.divider {
  width: 100%;
  height: 2px; /* Délka dělicí čáry */
  background-color: #F5F5DC  ; /* Barva čáry */
}
</style>