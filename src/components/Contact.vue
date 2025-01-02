<template>
  <section id="projects" class="pt-12 pb-1">
    <h2 class="text-3xl mb-8 text-center bg-blue-500 text-white px-16 py-3 rounded border font-semibold-bold hover:bg-blue-800 mg inline-block">Contact</h2>
    <div class="max-w-2xl mx-auto">
      <form @submit.prevent="handleSubmit" class="bg-white shadow-md rounded px-8 pt-6 pb-8 mb-4">
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="name">
            Name
          </label>
          <input v-model="form.name" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="name" type="text" placeholder="Your Name" required>
        </div>
        <div class="mb-4">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="email">
            Email
          </label>
          <input v-model="form.email" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="email" type="email" placeholder="your@email.com" required>
        </div>
        <div class="mb-6">
          <label class="block text-gray-700 text-sm font-bold mb-2" for="message">
            Message
          </label>
          <textarea v-model="form.message" class="shadow appearance-none border rounded w-full py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline" id="message" placeholder="Your message" rows="4" required></textarea>
        </div>
        <div class="flex items-center justify-between">
          <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded focus:outline-none focus:shadow-outline flex justify-center w-full" type="submit">
            Send Message
          </button>
        </div>
      </form>
      
      <div class="text-center">
        <p class="mb-4">Or reach out directly:</p>
        <a href="mailto:lhtthong.forwork@outlook.com"><p class="text-blue-600 mb-4">lhtthong.forwork@outlook.com</p></a>
        <div class="flex justify-center space-x-4">
          <a href="https://github.com/AlecVOV" target="_blank" rel="noopener noreferrer" class="text-gray-600 hover:text-blue-600">
            <GithubIcon class="w-6 h-6" />
          </a>
          <a href="https://linkedin.com/in/hoang-triet-thong-le-5b26b6185/" target="_blank" rel="noopener noreferrer" class="text-gray-600 hover:text-blue-600">
            <LinkedinIcon class="w-6 h-6" />
          </a>
          <a href="https://www.facebook.com/chilonthon" target="_blank" rel="noopener noreferrer" class="text-gray-600 hover:text-blue-600">
            <FacebookIcon class="w-6 h-6" />
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { defineComponent, reactive } from 'vue'
import { FacebookIcon, GithubIcon, LinkedinIcon} from 'lucide-vue-next'

export default defineComponent({
  name: 'Contact',
  components: {
    GithubIcon,
    LinkedinIcon,
    FacebookIcon
  },
  setup() {
    const form = reactive({
      name: '',
      email: '',
      message: ''
    })

    const handleSubmit = () => {
      // Here you would typically send the form data to a server
      console.log('Form submitted:', form)
      // Reset form after submission
      form.name = ''
      form.email = ''
      form.message = ''
      alert('Thank you for your message! We will get back to you soon.')
    }

    return {
      form,
      handleSubmit
    }
  }
})
</script>