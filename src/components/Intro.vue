<template>
  <section 
    ref="introSection"
    class="flex md:justify-end justify-center flex-col items-center text-center
           opacity-0 transform translate-y-10 transition-all duration-1200 px-10
           md:h-[600px] h-[400px] md:pb-30 md:min-h-[80vh]"
  >
    <h1 class="text-5xl font-bold md:text-6xl text-white tracking-wide">MY PORTFOLIO</h1>
    <p class="text-lg text-white mt-4 italic">A showcase of my projects and my SW Stack</p>
    <div class="mt-6"> 
      <a 
      href="#projects" 
      class="px-6 py-3 rounded-lg transition" 
      >
        <i class="fa-solid fa-circle-arrow-down fa-2xl text-gray text-gray-300"/>
      </a>
    </div>
  </section>
</template>

<script setup>
import { defineOptions, ref, onMounted } from 'vue';

defineOptions({
  name: "Inrto",
});

const introSection = ref(null);

onMounted(() => {
  const observer = new IntersectionObserver(
    ([entry]) => {
      if (entry.isIntersecting) {
        entry.target.classList.remove("translate-y-10");
        entry.target.classList.add("opacity-100", "translate-y-0");
      } else {
        entry.target.classList.remove("opacity-100", "translate-y-0");
        entry.target.classList.add("translate-y-10");
      }
    },
    { threshold: 0.9 }
  );

  if (introSection.value) observer.observe(introSection.value);
});

</script>

<style scoped>
.transition-all {
  will-change: transform, opacity;
}
</style>