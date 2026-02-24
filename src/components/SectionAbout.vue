<template>
  <section id="about" class="py-20 border-t border-white/5 mt-10">
    <div class="max-w-7xl mx-auto px-6">
      <div class="grid md:grid-cols-2 gap-16 items-center">
        
        <div class="relative group">
          <div
            class="aspect-square rounded-[2rem] overflow-hidden border border-white/10 relative bg-zinc-900 shadow-2xl"
          >
          
            <img
              src="../assets/perfil3.jpg"
              alt="Victor César"
              class="w-full h-full object-cover  object-[50%_10%] opacity-80 group-hover:opacity-100 group-hover:scale-105 transition-all duration-700 grayscale group-hover:grayscale-0"
              
            />
            <!-- @error="handleImageError" -->

            <!-- Gradiente sobre a foto para não ficar muito clara -->
            <div
              class="absolute inset-0 bg-gradient-to-t from-zinc-950 via-transparent to-transparent opacity-80 pointer-events-none"
            ></div>

           
            <div
              class="absolute bottom-6 left-6 px-4 py-2 border border-emerald-500/30 bg-black/50 backdrop-blur-md rounded-full"
            >
              <p
                class="text-emerald-400 text-xs font-bold tracking-widest uppercase"
              >
                IFBA • Sistemas de Informação
              </p>
            </div>
          </div>
          
          <div
            class="absolute -bottom-6 -right-6 w-32 h-32 bg-emerald-500/20 rounded-full blur-3xl -z-10 transition-all group-hover:bg-emerald-500/30"
          ></div>
        </div>

      
        <div>
          <h2
            class="text-4xl md:text-5xl font-bold mb-8 tracking-tight text-white"
          >
            Muito além do código.
          </h2>

          <div class="space-y-6 text-lg text-zinc-400 leading-relaxed">
            <p>
              Com mais de 3 anos de experiência prática, iniciei minha jornada
              na <strong class="text-zinc-200">BlockHub Builders</strong> e
              atuei no desenvolvimento de sistemas complexos de gestão de
              cartórios na <strong class="text-zinc-200">Vollare</strong>.
            </p>
            <p>
              Recentemente, expandi meus conhecimentos em
              <strong class="text-emerald-400">Ciência de Dados</strong> durante
              uma residência no CEPEDI. Essa visão analítica me permite entender
              não apenas "como" construir uma aplicação, mas "por que" ela deve
              ser construída.
            </p>
            <p>
              Como freelancer, meu foco não é apenas entregar linhas de código,
              mas fornecer
              <strong class="text-white"
                >soluções tecnológicas que resolvam problemas reais do seu
                negócio</strong
              >, garantindo escalabilidade, segurança e um design focado na
              experiência do usuário e na conversão.
            </p>

            
            <div class="pt-6 flex gap-6 border-t border-white/10 mt-8">
              <div class="flex flex-col gap-1">
                <span
                  class="text-4xl font-black text-white drop-shadow-[0_0_10px_rgba(255,255,255,0.2)]"
                  >3+</span
                >
                <span
                  class="text-sm text-zinc-500 font-mono uppercase tracking-wider"
                  >Anos de XP</span
                >
              </div>
              <div class="w-px h-16 bg-zinc-800"></div>
              <div class="flex flex-col gap-1">
                <span
                  class="text-4xl font-black text-white drop-shadow-[0_0_10px_rgba(255,255,255,0.2)]"
                  >Full</span
                >
                <span
                  class="text-sm text-zinc-500 font-mono uppercase tracking-wider"
                  >Stack</span
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "SectionAbout",
  setup() {
    const handleImageError = (e) => {
      if (e.target.style.display == "none") {
        e.target.parentNode.classList.add(
          "bg-[url('https://images.unsplash.com/photo-1534528741775-53994a69daeb?q=80&w=2000&auto=format&fit=crop')]",
          "bg-cover"
        );
      }
    };

    return {
      handleImageError,
    };
  },
};
</script>

<style scoped>

</style>
