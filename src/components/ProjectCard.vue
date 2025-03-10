<template>
  <article class="bg-gray-800 p-6 rounded-lg shadow-lg">
    <h3 class="text-xl font-semibold">{{ projectData.title }}</h3>
    <img 
      :src="projectData.image" 
      :alt="projectData.title" 
      class="rounded-lg mt-4 transition-transform duration-300 hover:scale-110"
    >
    <p class="text-gray-300 mt-4">{{ projectData.description }}</p>
    <div class="mt-4 flex space-x-4">
      <a 
        v-if="projectData?.production.url"
        :href="projectData.production.url" 
        target="_blank" 
        class="flex justify-center items-center text-center p-2 bg-blue-500 rounded-lg hover:bg-blue-600 transition"
      >
        <span>{{ projectData.production.title }}</span>
      </a>
      <a 
        v-for="(repo, index) in projectData.repositories"
        :key="repo+index"
        :href="repo.url"
        target="_blank" 
        class="flex justify-center items-center text-center p-2 bg-gray-600 rounded-lg hover:bg-gray-700 transition"
      >
        <span>{{ repo.title }}</span>
      </a>
    </div>
  </article>
</template>

<script setup>
import { defineOptions  } from 'vue';

defineOptions({
  name: "ProjectCard",
});

defineProps({
  projectData: {
    type: Object,
    default: ()=>{},
  },
})

</script>
