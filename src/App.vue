<template>
  <div class="font-sans antialiased">
    <!-- Header / Nav -->
    <Header />

    <!-- Main Content -->
    <main>
      <!-- Hero Section -->
      <Hero />

      <!-- About Me Section -->
      <!-- Reuse your existing AboutMe.vue. Make sure it has id="about-me" for anchor linking -->
      <AboutMe id="about-me" />

      <!-- Career Path Section-->
      <!-- Reuse your existing CareerPath.vue. Make sure it has id="about-me" for anchor linking -->
      <CareerPath id="career-path"/>

      <!-- Projects Section -->
      <!-- Reuse your existing Projects.vue. Make sure it has id="projects" for anchor linking -->
      <Projects id="projects" />

      <!-- Skills Section -->
      <!-- Reuse your existing Skills.vue. Make sure it has id="skills" for anchor linking -->
      <Skills id="skills" />

      <!-- Certifications Section -->
      <!-- Reuse your existing Certifications.vue. Make sure it has id="certifications" for anchor linking -->
      <Certifications id="certifications" />



      <!-- Contact Section -->
      <!-- Reuse your existing Contact.vue. Make sure it has id="contact" for anchor linking -->
      <Contact id="contact" />
    </main>

    <!-- Footer -->
    <Footer />
  </div>
</template>

<script lang="ts">
import { defineComponent } from 'vue'

// New Components
import Header from './components/Header.vue'
import Hero from './components/Hero.vue'
import Footer from './components/Footer.vue'

// Existing Components
import Projects from './components/Projects.vue'
import Skills from './components/Skills.vue'
import AboutMe from './components/AboutMe.vue'
import Contact from './components/Contact.vue'
import Certifications from './components/Certifications.vue'
// import CareerPath from './components/CareerPath.vue'


export default defineComponent({
  name: 'App',
  components: {
    Header,
    Hero,
    Footer,
    Projects,
    Skills,
    AboutMe,
    Contact, 
    Certifications,
  }
})
</script>

<style>
/* Global styles if needed. 
   Tailwind is typically used via @tailwind directives in your main CSS file. */
</style>
