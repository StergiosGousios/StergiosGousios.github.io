<template>
  <div class="relative bg-cover bg-center bg-[url('./MyImages/background.jpg')] pb-10 "> 
    <Intro/>
    <div class="min-h-screen bg-gray-900 text-white md:w-9/10 max-w-6xl m-auto z-1 relative">
      <NavBar :socialLinks="socialLinks"/>
      <About/>
      <Projects :projects="projects"/>
      <Footer :socialLinks="socialLinks"/>
    </div>
  </div>
</template>

<script setup>
import { projects, socialLinks } from '../projectData.js'
import { defineOptions } from 'vue';
import About from '../components/About.vue'
import Footer from '../components/Footer.vue'
import Intro from '../components/Intro.vue'
import Projects from '../components/Projects.vue'
import NavBar from '../components/NavBar.vue'

defineOptions({
  name: "HomeView",
});



</script>
