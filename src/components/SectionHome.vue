<template>
  <div>
    
    <section id="home" class="home-section min-h-[80vh] flex flex-col justify-center relative pt-20 lg:pt-32">
      
     
      <div class="flex items-center gap-4 mb-8 text-sm font-mono text-zinc-500">
        <div class="flex items-center gap-2 px-4 py-2 rounded-full border border-emerald-500/30 bg-emerald-500/10 shadow-[0_0_15px_rgba(16,185,129,0.15)]">
          <span class="relative flex h-2.5 w-2.5">
            <span class="animate-ping absolute inline-flex h-full w-full rounded-full bg-emerald-400 opacity-75"></span>
            <span class="relative inline-flex rounded-full h-2.5 w-2.5 bg-emerald-500"></span>
          </span>
          <span class="text-emerald-400 font-bold tracking-wide uppercase text-xs">Aceitando novos projetos</span>
        </div>
      </div>

    
      <h1 class="text-6xl md:text-8xl lg:text-9xl font-bold tracking-tighter leading-[0.9] mb-8 relative z-10">
        <span class="bg-gradient-to-b from-white via-white to-zinc-500 bg-clip-text text-transparent">VICTOR</span>
        <br />
        <span class="text-transparent bg-clip-text bg-gradient-to-r from-zinc-500 via-zinc-200 to-zinc-600 outline-text">CÉSAR.</span>
      </h1>


      <p class="text-lg md:text-2xl text-zinc-400 max-w-2xl leading-relaxed mb-12 border-l-2 border-emerald-500/50 pl-6">
        Desenvolvedor Web Full Stack. Transformo a sua ideia em um produto digital real. 
        Ajudo empresas e empreendedores a escalarem seus negócios com <span class="text-zinc-200 font-semibold">aplicações rápidas, modernas e sob medida</span>.
      </p>

   
      <div class="flex flex-wrap items-center gap-4 mt-4">
        
     
        <a href="#work" class="group flex items-center gap-3 px-8 py-4 bg-zinc-100 text-black font-bold rounded-full hover:bg-emerald-400 hover:scale-105 transition-all duration-300 shadow-[0_0_20px_rgba(255,255,255,0.1)]">
          Ver Portfólio
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="transition-transform group-hover:translate-x-1 group-hover:-translate-y-1"><path d="M7 7h10v10"/><path d="M7 17 17 7"/></svg>
        </a>

        <a href="#contact" class="px-8 py-4 border border-white/10 bg-white/5 backdrop-blur-sm text-white font-bold rounded-full hover:bg-white/10 transition-colors">
          Solicitar Orçamento
        </a>

        <div class="flex gap-4 ml-2">
          <a href="https://www.linkedin.com/in/victor-cesar-dev/" target="_blank" class="social-btn group" title="LinkedIn">
            <LinkedingSvg class="w-6 h-6 fill-zinc-400 group-hover:fill-white transition-colors" />
          </a>
          <a href="https://github.com/VeectorVt" target="_blank" class="social-btn group" title="GitHub">
            <GithubSvg class="w-6 h-6 fill-zinc-400 group-hover:fill-white transition-colors" />
          </a>
        </div>
        
      </div>

    </section>
  </div>
</template>

<script>

import GithubSvg from '../components/includes/github-svg.vue'
import LinkedingSvg from '../components/includes/linkedin-svg.vue'

export default {
  name: 'SectionHome',
  components: {
    GithubSvg,
    LinkedingSvg
  }
};
</script>

<style scoped>

.home-section {
  width: 100%;
}

.outline-text {
  -webkit-text-stroke: 1px rgba(255, 255, 255, 0.2);
  color: transparent;
}

.social-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1rem;
  background-color: rgba(255, 255, 255, 0.05); /* white/5 */
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 9999px;
  transition: all 0.3s ease;
}

.social-btn:hover {
  background-color: rgba(255, 255, 255, 0.1);
  transform: scale(1.1);
}

</style>