<template>
  <section id="hero" class="flex h-[80vh] w-full m-0 p-0 items-center">
    <!-- Image left -->
    <div
      class="w-1/2 bg-cover bg-left bg-no-repeat h-full"
      style="background-image: url('/my_image.jpg'); background-size: contain; background-position: left;"
    ></div>

    <!-- Text section aligned vertically center -->
    <div class="w-3/5 text-white p-10 flex items-center">
      <div class="max-w-xl">
        <h1 class="text-4xl md:text-4xl font-bold mb-4">Hello, Welcome to my website 🙌</h1>
        <p class="text-lg md:text-xl mb-6">Here you can explore my world, from an none fancy IT Developer, I would consider myself as a knowledge seeker by exploring new technologies and world insight about AI and related domain when applying up-to-date technologies into it. </p>
        <a href="#projects" class="bg-blue-400 text-white px-6 py-3 rounded font-semibold hover:bg-blue-700">
          View My Projects
        </a>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  name: 'Hero',
});
</script>
<style scoped>
/* Ensure the section is aligned to the left */
#hero {
  justify-content: flex-start;
}
</style>
