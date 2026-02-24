<template>
  <section id="skills" class="py-20 border-t border-white/5 mt-10">
    <div class="max-w-7xl mx-auto px-6">
      <div class="rounded-[2rem] bg-zinc-900/30 border border-white/5 p-8 md:p-12 relative overflow-hidden group hover:border-white/10 transition-colors">
        
       
        <div class="absolute top-0 right-0 p-12 opacity-5 pointer-events-none group-hover:opacity-10 transition-opacity duration-700">
           <Cpu :size="200" class="text-white" />
        </div>
        
        <div class="relative z-10">
          <h2 class="text-3xl font-bold mb-8 flex items-center gap-3 text-white">
            <Terminal class="text-emerald-500" /> 
            Arsenal Tecnológico
          </h2>
          
          <div class="grid grid-cols-2 md:grid-cols-4 gap-4">
            <div 
              v-for="tech in techStack" 
              :key="tech.name" 
              :class="['p-4 rounded-xl bg-white/5 border border-white/5 hover:bg-white/10 transition-all cursor-default group/tech', tech.border]"
            >
              <h3 :class="['font-bold text-lg transition-transform group-hover/tech:translate-x-1', tech.color]">
                {{ tech.name }}
              </h3>
              <p class="text-xs text-zinc-500 uppercase tracking-wider mt-1">{{ tech.level }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { Terminal, Cpu } from 'lucide-vue-next';

export default {
  name: "SectionSkills",
  components: {
    Terminal,
    Cpu
  },
  setup() {
    const techStack = [
      { name: 'Vue.js', level: 'Avançado', color: 'text-emerald-400', border: 'hover:border-emerald-500/30' },
      { name: 'Node.js', level: 'Intermediário', color: 'text-green-500', border: 'hover:border-green-500/30' },
      { name: 'React', level: 'Intermediário', color: 'text-blue-400', border: 'hover:border-blue-500/30' },
      { name: 'TypeScript', level: 'Intermediário', color: 'text-blue-500', border: 'hover:border-blue-500/30' },
      { name: 'Python', level: 'Básico', color: 'text-yellow-400', border: 'hover:border-yellow-500/30' },
      { name: 'Pandas', level: 'Data Science', color: 'text-indigo-400', border: 'hover:border-indigo-500/30' },
      { name: 'Tailwind CSS', level: 'Avançado', color: 'text-cyan-400', border: 'hover:border-cyan-500/30' },
      { name: 'MongoDB', level: 'Intermediário', color: 'text-green-600', border: 'hover:border-green-600/30' },
      { name: 'Cypress', level: 'Testing', color: 'text-zinc-400', border: 'hover:border-zinc-500/30' },
      { name: 'PostgreSQL', level: 'Básico', color: 'text-blue-300', border: 'hover:border-blue-300/30' },
    ];

    return {
      techStack
    };
  }
};
</script>

<style scoped>

</style>