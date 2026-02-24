<template>
  <section id="projects" class="py-20">
    <div class="max-w-7xl mx-auto px-6">
      
      <!-- Título da Secção -->
      <div class="flex items-end justify-between mb-12">
        <div>
          <h2 class="text-4xl font-bold tracking-tight mb-2 text-white">Projetos Selecionados</h2>
          <div class="h-1 w-20 bg-emerald-500 rounded-full"></div>
        </div>
        <span class="text-zinc-600 text-sm hidden md:flex items-center gap-2">
          <span class="w-2 h-2 rounded-full bg-emerald-500 animate-pulse"></span>
          Live Projects
        </span>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-6 gap-6 auto-rows-[320px]">
        
        <!-- 1. SISTEMA PARQUE (DESTAQUE GIGANTE - ESQUERDA) -->
        <div 
          @click="openProject('Sistema Parque', '', '')"
          class="group relative md:col-span-3 md:row-span-2 rounded-[2rem] overflow-hidden border border-white/10 bg-zinc-900 cursor-pointer shadow-2xl hover:shadow-emerald-900/20 transition-all duration-500 hover:border-emerald-500/30"
        >
          <div class="absolute inset-0 bg-gradient-to-br from-emerald-950/80 via-zinc-900/50 to-black z-0"></div>
          <div class="absolute inset-0 z-0">
             <img src="https://media.licdn.com/dms/image/v2/D4D22AQHwXXaGdVxyOg/feedshare-shrink_2048_1536/B4DZg.d44yH4Ao-/0/1753394680274?e=1773273600&v=beta&t=OUn1UQDTHIOMww8vX2qu68BCap1BVfg273fmNZjzzCo" alt="Sistema Parque Interface" class="w-full h-full object-cover object-[50%_50%] opacity-80 group-hover:scale-105 group-hover:opacity-100 transition-all duration-700" @error="handleImageError" />
          </div>
          <div class="absolute top-6 right-6 z-20">
            <div class="p-3 bg-emerald-500/20 backdrop-blur-md rounded-full border border-emerald-500/30 text-emerald-400 group-hover:bg-emerald-500 group-hover:text-black transition-all shadow-lg">
              <LayoutGrid :size="24" />
            </div>
          </div>
          <div class="absolute bottom-0 left-0 p-8 md:p-12 w-full bg-gradient-to-t from-black via-zinc-950/90 to-transparent z-20">
            <span class="inline-block px-3 py-1 rounded-full bg-emerald-500/20 border border-emerald-500/20 text-emerald-400 text-xs font-bold tracking-wider mb-3">SISTEMA DE GESTÃO(Sistema Interno)</span>
            <h3 class="text-4xl md:text-5xl font-bold text-white mb-3 group-hover:text-emerald-200 transition-colors shadow-black drop-shadow-lg">Parque</h3>
            <p class="text-zinc-200 line-clamp-2 md:line-clamp-3 mb-6 text-lg max-w-2xl leading-relaxed drop-shadow-md">Sistema completo para gestão de lotes e administração imobiliária. Controle de status, proprietários e visualização em tempo real de ocupação com foco em performance e usabilidade.</p>
            <div class="flex flex-wrap gap-2">
              <span v-for="tag in ['Vue.js', 'Node.js', 'PostgreSQL', 'Tailwind']" :key="tag" class="text-xs font-mono bg-black/40 backdrop-blur border border-white/10 text-zinc-300 px-3 py-1.5 rounded-lg group-hover:border-emerald-500/30 transition-colors">{{ tag }}</span>
            </div>
          </div>
        </div>

        <!-- 2. LANDING PAGE 1 -->
        <div 
          @click="openProject('Sc clin premium', 'https://github.com/VeectorVt/Sc-clin-premium', 'https://sc-clin-premium.vercel.app/')"
          class="group relative md:col-span-3 md:row-span-2 rounded-[2rem] overflow-hidden border border-white/10 bg-zinc-900 cursor-pointer hover:border-orange-500/30 transition-all"
        >
          <div class="absolute inset-0 z-0">
            
             <img src="../assets/sc-clin-premium.png" alt="SC CLIN PREMIUM" class="w-full h-full object-cover opacity-70 group-hover:scale-105 group-hover:opacity-100 transition-all duration-700" @error="handleImageError" />
          </div>
        
          <div class="absolute inset-0 bg-gradient-to-t from-black via-black/60 to-transparent z-10"></div>
          <div class="absolute bottom-0 left-0 p-8 w-full z-20">
             <span class="text-[10px] bg-orange-500/20 text-orange-300 px-2 py-1 rounded uppercase tracking-wide border border-orange-500/30 mb-2 inline-block">Landing Page</span>
             <h3 class="text-3xl font-bold text-white mb-2 drop-shadow-lg leading-tight">SC CLIN PREMIUM</h3>
             <p class="text-zinc-300 text-sm leading-relaxed drop-shadow-md line-clamp-3"></p>
          </div>
        </div>

        <!-- 3. LANDING PAGE 2 -->
        <div 
          @click="openProject('SC CLIN ', '', 'https://sc-clin-landing-flow.vercel.app/')"
          class="group relative md:col-span-3 md:row-span-1 rounded-[2rem] overflow-hidden border border-white/10 bg-zinc-900 cursor-pointer hover:border-teal-500/30 transition-all"
        >
          <div class="absolute inset-0 z-0">
      
             <img src="../assets/landing-flow.png" alt="Clínica Vitality" class="w-full h-full object-cover  opacity-60 group-hover:scale-105 group-hover:opacity-90 transition-all duration-700" />
          </div>
          <div class="absolute inset-0 bg-gradient-to-t from-black via-black/50 to-transparent z-10"></div>
          <div class="absolute bottom-0 left-0 p-8 w-full z-20">
             <span class="text-[10px] bg-teal-500/20 text-teal-300 px-2 py-1 rounded uppercase tracking-wide border border-teal-500/30 mb-2 inline-block">Clínica de Fisioterapia</span>
             <h3 class="text-2xl font-bold text-white mb-1 drop-shadow-lg">SC - Clin Fisio</h3>
             <p class="text-zinc-300 text-sm leading-relaxed drop-shadow-md line-clamp-2">Site institucional moderno e otimizado para captação de pacientes e agendamento de consultas.</p>
          </div>
        </div>

        <!-- 4. LANDING PAGE 3 -->
        <div 
          @click="openProject('DOG CAT MIMO', 'https://github.com/VeectorVt/landing-page-dog-cat', '')"
          class="group relative md:col-span-3 md:row-span-1 rounded-[2rem] overflow-hidden border border-white/10 bg-zinc-900 cursor-pointer hover:border-pink-500/30 transition-all"
        >
          <div class="absolute inset-0 z-0">
          
             <img src="../assets/dog-cat.png" alt="Fisio Life" class="w-full h-full object-cover opacity-60 group-hover:scale-105 group-hover:opacity-90 transition-all duration-700" />
          </div>
          <div class="absolute inset-0 bg-gradient-to-t from-black via-black/50 to-transparent z-10"></div>
          <div class="absolute bottom-0 left-0 p-8 w-full z-20">
             <span class="text-[10px] bg-pink-500/20 text-pink-300 px-2 py-1 rounded uppercase tracking-wide border border-pink-500/30 mb-2 inline-block">Bem Estar</span>
             <h3 class="text-2xl font-bold text-white mb-1 drop-shadow-lg">Dog Cat Mimo</h3>
             <p class="text-zinc-300 text-sm leading-relaxed drop-shadow-md line-clamp-2">Página de alta conversão desenhada para um infoproduto focado na saúde e bem-estar de cães e gatos.</p>
          </div>
        </div>

        <!-- 5. VOLLARE CARTÓRIOS (MINIMALISTA) -->
        <div 
          @click="openProject('Vollare Cartórios', '', '')"
          class="group relative md:col-span-3 md:row-span-1 rounded-[2rem] overflow-hidden border border-white/5 bg-zinc-900/40 cursor-pointer hover:bg-zinc-900 hover:border-blue-500/30 transition-all flex flex-col justify-between p-8"
        >
          
          <div class="absolute inset-0 bg-gradient-to-br from-blue-900/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"></div>
          
          <div class="flex justify-between items-start z-10">
            <div class="p-3 bg-blue-500/10 rounded-xl border border-blue-500/20">
              <Briefcase :size="24" class="text-blue-400" />
            </div>
            <span class="text-xs font-mono text-zinc-500 border border-zinc-800 bg-zinc-950 px-3 py-1 rounded-full group-hover:border-blue-500/30 transition-colors">Sistema Interno</span>
          </div>

          <div class="z-10 mt-6">
             <h3 class="text-2xl font-bold text-white mb-2 group-hover:text-blue-200 transition-colors">Vollare Cartórios</h3>
             <p class="text-zinc-400 text-sm leading-relaxed mb-4">Desenvolvimento e manutenção de sistema complexo para gestão de fluxos cartorários. Criação de telas com Vue.js e implementação de testes E2E.</p>
             <div class="flex flex-wrap gap-2">
                <span class="text-[10px] uppercase tracking-wider text-blue-300 bg-blue-500/10 px-2 py-1 rounded">Vue.js</span>
                <span class="text-[10px] uppercase tracking-wider text-blue-300 bg-blue-500/10 px-2 py-1 rounded">Vuex</span>
                <span class="text-[10px] uppercase tracking-wider text-blue-300 bg-blue-500/10 px-2 py-1 rounded">Cypress</span>
             </div>
          </div>
        </div>

        <!-- 6. DATA SCIENCE CEPEDI (MINIMALISTA) -->
        <div 
          class="group relative md:col-span-3 md:row-span-1 rounded-[2rem] overflow-hidden border border-white/5 bg-zinc-900/40 hover:bg-zinc-900 hover:border-purple-500/30 transition-all flex flex-col justify-between p-8"
        >
          <div class="absolute inset-0 bg-gradient-to-tl from-purple-900/10 to-transparent opacity-0 group-hover:opacity-100 transition-opacity"></div>
          
          <div class="flex justify-between items-start z-10">
            <div class="p-3 bg-purple-500/10 rounded-xl border border-purple-500/20">
              <Database :size="24" class="text-purple-400" />
            </div>
            <span class="text-xs font-mono text-zinc-500 border border-zinc-800 bg-zinc-950 px-3 py-1 rounded-full group-hover:border-purple-500/30 transition-colors">Residência</span>
          </div>

          <div class="z-10 mt-6">
             <h3 class="text-2xl font-bold text-white mb-2 group-hover:text-purple-200 transition-colors">CEPEDI Data Science</h3>
             <p class="text-zinc-400 text-sm leading-relaxed mb-4">Participação em residência de software focada em análise e manipulação de conjuntos de dados, criando visualizações e scripts focados em tomada de decisão.</p>
             <div class="flex flex-wrap gap-2">
                <span class="text-[10px] uppercase tracking-wider text-purple-300 bg-purple-500/10 px-2 py-1 rounded">Python</span>
                <span class="text-[10px] uppercase tracking-wider text-purple-300 bg-purple-500/10 px-2 py-1 rounded">Pandas</span>
                <span class="text-[10px] uppercase tracking-wider text-purple-300 bg-purple-500/10 px-2 py-1 rounded">Matplotlib</span>
             </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script>
import { LayoutGrid, Briefcase, Database } from 'lucide-vue-next';
import Swal from 'sweetalert2';

export default {
  name: "SectionProjects",
  components: {
    LayoutGrid,
    Briefcase,
    Database,
    // BarChart3
  },
  setup() {
    const handleImageError = (e) => {
     
      e.target.src = 'https://images.unsplash.com/photo-1618005182384-a83a8bd57fbe?q=80&w=2564&auto=format&fit=crop';
    };

    const openProject = (title, repoUrl, liveUrl) => {
      if (!repoUrl && !liveUrl) {
        Swal.fire({
          title: 'Projeto Privado / Em breve',
          text: 'Este projeto é confidencial ou os links ainda não foram disponibilizados.',
          icon: 'info',
          background: '#09090b',
          color: '#f4f4f5',
          confirmButtonColor: '#10b981'
        });
        return;
      }

      Swal.fire({
        html: liveUrl
          ? `<h3 style='font-family: Saira, sans-serif; font-size: 1.5rem; margin-bottom: 10px;'>Onde deseja visualizar o projeto <b>${title}</b>?</h3>`
          : `<h3 style='font-family: Saira, sans-serif; font-size: 1.5rem; margin-bottom: 10px;'>Deseja ir para o repositório de <b>${title}</b>?</h3>`,
        showConfirmButton: !!liveUrl,
        showDenyButton: !!repoUrl,
        showCancelButton: true,
        confirmButtonText: "Ver Aplicação",
        denyButtonText: "Ver Código (GitHub)",
        cancelButtonText: "Cancelar",
        confirmButtonColor: "#10b981", 
        denyButtonColor: "#3f3f46", 
        cancelButtonColor: "#ef4444", 
        background: "#09090b", 
        color: "#f4f4f5", 
        customClass: {
          popup: 'border border-white/10 rounded-2xl'
        }
      }).then((result) => {
        if (result.isConfirmed && liveUrl) {
          window.open(liveUrl, "_blank");
        } else if (result.isDenied && repoUrl) {
          window.open(repoUrl, "_blank");
        }
      });
    };

    return {
      handleImageError,
      openProject
    };
  }
};
</script>

<style scoped>

</style>