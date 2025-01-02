<!-- <template>
  <section id="skills" class="py-12">
    <h2 class="text-3xl mb-8 text-center bg-blue-500 text-white px-16 py-3 rounded border font-semibold-bold hover:bg-blue-800 mg inline-block">Skills</h2>
    <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mx-8">
      <div v-for="category in skillCategories" :key="category.name" class="bg-white rounded-lg shadow-md p-6">
        <h3 class="text-xl font-semibold mb-4">{{ category.name }}</h3>
        <ul class="space-y-2">
          <li v-for="skill in category.skills" :key="skill.name" class="flex items-center">
            <component :is="skill.icon" class="w-6 h-6 mr-2" />
            <span>{{ skill.name }}</span>
            <div class="ml-auto w-24 bg-gray-200 rounded-full h-2">
              <div class="bg-blue-600 rounded-full h-2" :style="{ width: `${skill.proficiency}%` }"></div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template> -->

<script lang="ts">
import { defineComponent } from 'vue'
import { Code, Database, Palette, type LucideIcon } from 'lucide-vue-next'

interface Skill {
  name: string;
  icon: LucideIcon;  
  proficiency: number;
}

interface SkillCategory {
  name: string;
  skills: Skill[];
}

export default defineComponent({
  name: 'Skills',
  components: {
    Code,
    Database,
    Palette
  },
  setup() {
    const skillCategories: SkillCategory[] = [
      {
        name: 'Frontend',
        skills: [
          { name: 'Vue.js', icon: Code, proficiency: 90 },
          { name: 'React', icon: Code, proficiency: 85 },
          { name: 'TypeScript', icon: Code, proficiency: 80 },
          { name: 'CSS/Sass', icon: Palette, proficiency: 85 }
        ]
      },
      {
        name: 'Backend',
        skills: [
          { name: 'Node.js', icon: Code, proficiency: 80 },
          { name: 'Python', icon: Code, proficiency: 75 },
          { name: 'SQL', icon: Database, proficiency: 70 },
          { name: 'MongoDB', icon: Database, proficiency: 65 }
        ]
      },
      {
        name: 'Tools & Others',
        skills: [
          { name: 'Git', icon: Code, proficiency: 85 },
          { name: 'Docker', icon: Code, proficiency: 70 },
          { name: 'AWS', icon: Code, proficiency: 60 },
          { name: 'Figma', icon: Palette, proficiency: 75 }
        ]
      }
    ]

    return { skillCategories }
  }
})
</script>