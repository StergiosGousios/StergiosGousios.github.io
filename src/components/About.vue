<template>
  <div class="flex justify-center flex-col items-center max-w-5xl mx-auto px-6 text-center">
    <h1 class="py-10 text-4xl font-semibold ">Stergios Gousios</h1>
    <div class="text-merriweather">
      <p class="text-gray-300 mt-4">
        Welcome to my Portfolio page. I am Stergios, a Software Engineer passionate about web programming.
        I like to work with modern front-end technologies and frameworks to build scalable web applications and user interfaces.
      </p>
      <p class="text-gray-300 mt-4">
        Feel free to look around, browse my projects and contact me via LinkedIn or email to grant you access to my private repositories.
      </p>
    </div>
  </div>
</template>

<script setup>
import { defineOptions  } from 'vue';

defineOptions({
  name: "About",
});

</script>

<style scoped>
.text-merriweather {
  font-family: ‘Merriweather’, Georgia, serif;
}
</style>
