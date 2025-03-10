<template>
  <footer class="mt-16 text-center">
    <div class="text-lg font-semibold">Contact</div>
    <div class="text-gray-400 mt-4">Email: gousios.stergios@gmail.com</div>
    <div class="mt-4 flex justify-center space-x-4">
      <a 
        v-for="(link, index) in socialLinks" 
        :key="'footerLink-'+index"
        :href="link.href" 
        target="_blank" 
        class="hover:text-blue-400 transition"
      >
        <i :class="link.icon" class="text-2xl"/>
      </a>
    </div>
    <div class="text-gray-500 mt-4 pb-4">© 2025 Stergios Gousios</div>
  </footer>
</template>

<script setup>
import { defineOptions, defineProps } from 'vue';

defineOptions({
  name: "Footer",
});

defineProps({
  socialLinks: {
    type: Array,
    default: ()=>[],
  },
})

</script>
