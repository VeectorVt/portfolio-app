<template>
  <div class="min-h-screen bg-zinc-950 text-zinc-100 font-sans selection:bg-emerald-500/30 selection:text-emerald-200 overflow-x-hidden">
    
   
    <NavbarHome />

  
    <main>
      <SectionHome />
      <SectionAbout />
      <SectionProjects />
      <SectionSkills />
    </main>

    
    <footer id="contact" class="py-32 text-center relative overflow-hidden border-t border-white/5 mt-20">
      
      
      <div class="absolute top-1/2 left-1/2 -translate-x-1/2 -translate-y-1/2 w-[600px] h-[600px] bg-emerald-500/5 rounded-full blur-[120px] -z-10 pointer-events-none"></div>
      
      <h2 class="text-5xl md:text-7xl font-bold tracking-tighter mb-8 text-white">
        Vamos construir <br /> <span class="text-zinc-600">o futuro.</span>
      </h2>
      
      <div class="flex flex-col items-center gap-6">
        <p class="text-zinc-400 mb-2">Pronto para dar vida à sua ideia?</p>
        
        <a href="mailto:victorocalheiros@outlook.com" class="text-xl md:text-3xl text-zinc-300 hover:text-emerald-400 transition-colors border-b border-zinc-700 hover:border-emerald-400 pb-2">
          victorocalheiros@outlook.com
        </a>

        <!-- Redes Sociais no Footer usando SVGs Inline -->
        <div class="flex gap-4 mt-8">
          <a href="https://github.com/VeectorVt" target="_blank" title="GitHub" class="w-14 h-14 rounded-full bg-zinc-900 border border-white/10 flex items-center justify-center text-zinc-400 hover:text-white hover:bg-black hover:scale-110 transition-all shadow-xl group">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="group-hover:stroke-white"><path d="M15 22v-4a4.8 4.8 0 0 0-1-3.5c3 0 6-2 6-5.5.08-1.25-.27-2.48-1-3.5.28-1.15.28-2.35 0-3.5 0 0-1 0-3 1.5-2.64-.5-5.36-.5-8 0C6 2 5 2 5 2c-.3 1.15-.3 2.35 0 3.5A5.403 5.403 0 0 0 4 9c0 3.5 3 5.5 6 5.5-.39.49-.68 1.05-.85 1.65-.17.6-.22 1.23-.15 1.85v4"/><path d="M9 18c-4.51 2-5-2-7-2"/></svg>
          </a>
          <a href="https://www.linkedin.com/in/victor-cesar-dev/" target="_blank" title="LinkedIn" class="w-14 h-14 rounded-full bg-zinc-900 border border-white/10 flex items-center justify-center text-zinc-400 hover:text-blue-500 hover:bg-black hover:scale-110 transition-all shadow-xl group">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="group-hover:stroke-blue-500"><path d="M16 8a6 6 0 0 1 6 6v7h-4v-7a2 2 0 0 0-2-2 2 2 0 0 0-2 2v7h-4v-7a6 6 0 0 1 6-6z"/><rect width="4" height="12" x="2" y="9"/><circle cx="4" cy="4" r="2"/></svg>
          </a>
        </div>
      </div>

      <p class="mt-24 text-sm text-zinc-600 font-mono uppercase tracking-wider">
        © {{ currentYear }} / Victor César / Todos os direitos reservados
      </p>
    </footer>

  </div>
</template>

<script>

import NavbarHome from "../components/NavbarHome.vue";
import SectionHome from "../components/SectionHome.vue";
import SectionAbout from "../components/SectionAbout.vue";
import SectionProjects from "../components/SectionProjects.vue";
import SectionSkills from "../components/SectionSkills.vue";

export default {
  name: "HomePage",
  components: {
    NavbarHome,
    SectionHome,
    SectionAbout,
    SectionProjects,
    SectionSkills,
  },
  setup() {
   
    const currentYear = new Date().getFullYear();

    return {
      currentYear
    };
  },
};
</script>

<style scoped>

</style>