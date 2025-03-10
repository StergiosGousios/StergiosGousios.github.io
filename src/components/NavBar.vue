<template>
  <div class=" bg-gray-800 py-4 max-w-6xl flex justify-between items-center px-6">
      <div class="text-xl text-white font-semibold">Projects</div>
      <div class="flex justify-center  space-x-4"> 
        <a 
          v-for="(link, index) in socialLinks" 
          :key="'navbarLink-'+index"
          :href="link.href" 
          target="_blank" 
          class="hover:text-blue-400 transition"
        >
          <i :class="link.icon" class="text-2xl"/>
        </a>
      </div>
  </div> 
</template>

<script setup>
import { defineOptions, defineProps } from 'vue';

defineOptions({
  name: "NavBar",
});

defineProps({
  socialLinks: {
    type: Array,
    default: ()=>[],
  },
})
</script>
