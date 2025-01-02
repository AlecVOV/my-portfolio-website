<template>
  <section id="projects" class="py-12">
    <a href="https://github.com/AlecVOV?tab=repositories"><h2 class="text-3xl mb-8 text-center bg-blue-500 text-white px-16 py-3 rounded border font-semibold-bold hover:bg-blue-800 mg inline-block">Projects</h2></a>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mx-8">
      <div v-for="project in projects" :key="project.id" class="bg-white rounded-lg shadow-md overflow-hidden">
        <img :src="project.image" :alt="project.title" class="w-full h-auto object-cover">
        <div class="pr-6 pb-6 pl-6">
          <h3 class="text-xl font-semibold mb-2">{{ project.title }}</h3>
          <p class="text-gray-600 mb-4">{{ project.description }}</p>
          <div class="flex flex-wrap gap-2 mb-4 text-black">
            <span v-for="tech in project.technologies" :key="tech" class="bg-gray-200 hover:bg-[rgb(59,130,246)] text-sm px-2 py-1 rounded transition-all duration-300 ease-in-out"> 
              {{ tech }}
            </span>
          </div>
          <div class="flex justify-between">
            <a :href="project.demo" target="_blank" rel="noopener noreferrer" class="text-blue-600 hover:underline">Live Demo</a>
            <a :href="project.repo" target="_blank" rel="noopener noreferrer" class="text-blue-600 hover:underline">Repository</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

interface Project {
  id: number;
  title: string;
  description: string;
  image: string;
  technologies: string[];
  demo: string;
  repo: string;
}

export default defineComponent({
  name: 'Projects',
  setup() {
    const projects: Project[] = [
      {
        id: 1,
        title: 'Project 1',
        description: 'Snake game built with Python and Pygame.',
        image: '/snake_game_logo.webp',
        technologies: ['Python', 'Pygame Library',],
        demo: 'https://example.com/demo1',
        repo: 'https://github.com/AlecVOV/Self-Project/tree/main/Snake%20Game%20Project'
      },
      // Add more projects as needed
    ]

    return { projects }
  }
})
</script>