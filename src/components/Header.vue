<template>
    <header class="bg-white shadow-md">
      <div class="container mx-auto flex items-center justify-between py-4 px-6">
        <!-- Logo / Title -->
        <div class="text-xl font-bold text-blue-600">My Portfolio</div>
        
        <!-- Navigation Menu -->
        <nav class="hidden md:block ml-auto">
          <ul class="flex space-x-4">
            <li>
              <a href="#hero" class="hover:text-blue-800 transition-colors">
                Home
              </a>
            </li>
            <li>
              <a href="#projects" class="hover:text-blue-800 transition-colors">
                Projects
              </a>
            </li>
            <li>
              <a href="#skills" class="hover:text-blue-800 transition-colors">
                Skills
              </a>
            </li>
            <li>
              <a href="#about-me" class="hover:text-blue-800 transition-colors">
                About Me
              </a>
            </li>
            <li>
              <a href="#contact" class="hover:text-blue-800 transition-colors">
                Contact
              </a>
            </li>
            <li>
              <a href="#certifications" class="hover:text-blue-800 transition-colors">
                Certifications
              </a>
            </li>
          </ul>
        </nav>
      </div>
    </header>
</template>
  
  <script lang="ts">
  import { defineComponent } from 'vue'
  
  export default defineComponent({
    name: 'Header'
  })
  </script>
  
  <style scoped>
  /* You can add additional styling if you want */
  </style>
