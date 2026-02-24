<template>
  
  <nav :class="[
    'fixed top-0 left-0 right-0 z-50 transition-all duration-500',
    scrolled ? 'py-4 bg-zinc-950/80 backdrop-blur-xl border-b border-white/5 shadow-lg shadow-black/20' : 'py-8 bg-transparent'
  ]">
    <div class="max-w-7xl mx-auto px-6 flex justify-between items-center">
      
      <!-- Logo -->
      <a href="#home" class="text-xl font-bold tracking-tighter hover:text-white transition-colors cursor-pointer uppercase flex items-center gap-2 decoration-transparent">
        <div class="w-8 h-8 bg-gradient-to-br from-blue-500 to-zinc-800 rounded-lg flex items-center justify-center text-xs font-black border border-white/10 shadow-[0_0_15px_#60A5FA]">
          VC
        </div>
        Victor César
      </a>
      
  
      <div class="hidden md:flex gap-8 text-sm font-medium text-zinc-400 bg-white/5 px-6 py-2 rounded-full border border-white/5 backdrop-blur-md">
        <a href="#home" class="hover:text-emerald-400 transition-colors decoration-transparent">Início</a>
        <a href="#about" class="hover:text-emerald-400 transition-colors decoration-transparent">Sobre Mim</a>
        <a href="#projects" class="hover:text-emerald-400 transition-colors decoration-transparent">Projetos</a>
        <a href="#skills" class="hover:text-emerald-400 transition-colors decoration-transparent">Skills</a>
      </div>

     
      <a href="#contact" class="px-5 py-2 bg-zinc-100 text-black text-sm font-bold rounded-full hover:bg-emerald-400 hover:scale-105 transition-all shadow-[0_0_20px_rgba(255,255,255,0.1)] decoration-transparent">
        Fale Comigo
      </a>

    </div>
  </nav>
</template>

<script>
import { ref, onMounted, onUnmounted } from 'vue';

export default {
  name: "NavbarHome",
  setup() {
    const scrolled = ref(false);

    const handleScroll = () => {
      scrolled.value = window.scrollY > 50;
    };

    onMounted(() => {
      window.addEventListener('scroll', handleScroll);
    });

    onUnmounted(() => {
      window.removeEventListener('scroll', handleScroll);
    });

    return {
      scrolled
    };
  }
};
</script>

<style scoped>

</style>