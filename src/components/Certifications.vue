<template>
    <section id="certifications" class="py-12">
      <h2 class="text-3xl mb-8 text-center bg-blue-500 text-white px-16 py-3 rounded border font-semibold-bold hover:bg-blue-800 mg inline-block">Certifications</h2>
      <div class="max-w-4xl mx-auto">
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">  
          <div v-for="cert in certifications" :key="cert.id" class="bg-white rounded-lg shadow-md p-6">
            <h3 class="text-gray-600 text-xl font-semibold mb-2">{{ cert.name }}</h3>
            <p class="text-gray-600 mb-1">{{ cert.issuer }}</p>
            <p class="text-gray-500">{{ cert.date }}</p>
            <a :href="cert.link" target="_blank" rel="noopener noreferrer" class="text-blue-600 hover:underline mt-4 inline-block">View Certificate</a>
          </div>
        </div>
      </div>
    </section>
</template>
  
  <script lang="ts">
  import { defineComponent } from 'vue'
  
  interface Certification {
    id: number;
    name: string;
    issuer: string;
    date: string;
    link: string;
  }
  
  export default defineComponent({
    name: 'Certifications',
    setup() {
      const certifications: Certification[] = [
        {
          id: 1,
          name: 'CCNA: Introduction to Networks',
          issuer: 'Cisco',
          date: 'April 2024',
          link: 'https://www.credly.com/badges/ea475619-7376-44f1-9bba-162b836b9c48'
        },
        {
          id: 2,
          name: 'Programming for Everybody (Getting Started with Python)',
          issuer: 'University of Michigan',
          date: 'October 2024',
          link: 'https://coursera.org/share/5ee62f4961be5e83b3d118d4ef28e6a6'
        },
        {
          id: 3,
          name: 'AWS Academy Graduate - AWS Academy Cloud Foundations',
          issuer: 'Amazon Web Services',
          date: 'October 2024',
          link: 'https://www.credly.com/badges/988c98b4-6507-4e49-b2d2-6093db2310fa'
        },
        {
          id: 4,
          name: 'Getting Started with Data Analytics on AWS',
          issuer: 'Amazon Web Services',
          date: 'December 2024',
          link: 'https://coursera.org/share/d50e9b9c27fafd6c418db51ff6c888f9'
        }
        // Add more certifications as needed
      ]
  
      return { certifications }
    }
  })
  </script>
  
  <style scoped>
  /* Add any additional styles if needed */
  </style>