<template>
  <section id="projects" class="mt-16 max-w-5xl mx-auto md:px-6">
    <h2 class="text-3xl font-bold text-center mb-8">Projects</h2>
    <ProjectCard
      class="mb-8"
      :key="projects[0].id"
      :projectData="projects[0]"
    />
    <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-8">
      <ProjectCard
        v-for="(project, index) in filteredProjects"
        :key="project.id"
        :projectData="project"
        :shouldDisplayLarge="!!index"
      />
    </div>
  </section>
</template>

<script setup>
import { defineOptions , defineProps, computed } from 'vue';
import ProjectCard from '../components/ProjectCard.vue'

defineOptions({
  name: "Projects",
});

const props = defineProps({
  projects: {
    type: Array,
    default: ()=>[],
  },
})

const filteredProjects = computed(() => (props.projects.slice(1)));
</script>
