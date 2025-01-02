<!-- <template>
  <section id="career-path" class="py-12">
    <h2 class="text-3xl mb-8 text-center bg-blue-500 text-white px-16 py-3 rounded border font-semibold-bold hover:bg-blue-800 mg inline-block">About Me</h2>
    <div class="flex flex-col md:flex-row items-center md:items-start gap-8">
      <img src="/my_image2.jpg?height=300&width=300" alt="Le Hoang Triet Thong" class="pl-5 w-64 h-64 rounded-full object-cover shadow-lg">
      <div class="pl-8">
        <h3 class="text-2xl md:text-4xl font-semibold mb-4 ">Le Hoang Triet Thong</h3>
        <p class="text-gray-700 mb-6">
          I’m an undergraduate pursuing a degree in Computer Science – AI, complemented by specialized coursework in Data Science and Artificial Intelligence. 
          My academic journey gives me a theoretical grounding in cloud computing, machine learning, and software development, while my hands-on projects have challenged me to apply that knowledge in real-world scenarios.
        </p>
        <h4 class="text-xl font-semibold mb-4">Career Timeline</h4>
        <ul class="space-y-4">
          <li v-for="(event, index) in careerTimeline" :key="index" class="flex">
            <div class="mr-4 flex flex-col items-center">
              <div class="w-3 h-3 bg-blue-600 rounded-full"></div>
              <div class="w-0.5 h-full bg-blue-600"></div>
            </div>
            <div>
              <h5 class="text-lg font-semibold">{{ event.title }}</h5>
              <p class="text-gray-600">{{ event.date }}</p>
              <p class="text-gray-700">{{ event.description }}</p>
            </div>
          </li>
        </ul> 
      </div>
    </div>
  </section>
</template>  -->


<script lang="ts">
import { defineComponent } from 'vue'

interface CareerEvent {
  title: string;
  date: string;
  description: string;
}

export default defineComponent({
  name: 'AboutMe',
  setup() {
    const careerTimeline: CareerEvent[] = [
      // {
      //   title: 'Senior Frontend Developer',
      //   date: '2021 - Present',
      //   description: 'Leading frontend development for a major SaaS platform, focusing on performance optimization and accessibility.'
      // },
      // {
      //   title: 'Full Stack Developer',
      //   date: '2018 - 2021',
      //   description: 'Worked on various projects using Vue.js, Node.js, and AWS, delivering scalable web applications.'
      // },
      // {
      //   title: 'Junior Web Developer',
      //   date: '2016 - 2018',
      //   description: 'Started my career working on responsive websites and e-commerce platforms using HTML, CSS, and JavaScript.'
      // }
    ]
    return { careerTimeline }
  }
})
</script>
