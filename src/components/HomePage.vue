<template>
  <div v-if="initialPage" class="initialPage">
    <div data-aos-delay="1020" data-aos="flip-up" class="content-initial">
      <h1>Seja Bem Vindo ao Portfólio Infinito &#9854;</h1>
      <h4>
        Não por que ele é infinito em si , <br />
        mas está em desenvolvimento infinito ! <br />
        (e talvez algum dia se torne , de fato infinito...)&#9854;
      </h4>

      <!-- <h4 style="text-align: center;">Em breve:</h4>
      <p style="text-align: left;">-Responsividade para dispositivos Mobile</p> -->

      <button @click="changeSections" type="button" class="btn btn-primary lg">
        Continuar
      </button>
    </div>


    <div  class="content-initial mt-5">
    <div>
    
      <h4 style="text-align: center;">Em breve:</h4>
      <p style="text-align: left;">-Responsividade para dispositivos Mobile</p>

    </div>
  </div>

  </div>

  
  <div v-if="!swalWelcome && !initialPage" class="home-page">
    <!-- Início  Navbar -->
    <NavbarHome />

    <div class="sections">
      <!-- Home -->
      <SectionHome data-aos-delay="1020" data-aos="fade-left" id="home" />
      <!-- Sobre mim -->
      <SectionAbout data-aos-delay="1020" data-aos="fade-right" id="about" />

      <SectionProjects
        data-aos-delay="1020"
        data-aos="fade-up-left"
        id="projects"
      />

      <SectionSkills data-aos-delay="1020" data-aos="fade-down" id="skills" />
    </div>

    <footer data-aos-delay="1020" data-aos="fade-down" data-aos-once="true">
      <h1
        data-aos="zoom-out-up"
        data-aos-duration="3000"
        data-aos-once="true"
        data-aos-delay="2500"
      >
        Parabéns você chegou ao fim do Portfólio "infinito" &#9854; ! &#129300;
      </h1>
      <div class="contato">
        <div
          class="email"
          data-aos="zoom-out-up"
          data-aos-once="true"
          data-aos-delay="500"
          data-aos-duration="2000"
        >
          <h2>Email para contato</h2>
          <p>victorocalheiros@outlook.com</p>
        </div>
        <div
          class="redes"
          data-aos="zoom-out-up"
          data-aos-once="true"
          data-aos-delay="1500"
          data-aos-duration="2000"
        >
          <h2>Veja mais em:</h2>

          <div class="linkedin">
            <a href="https://www.linkedin.com/in/victor-cesar-dev/" target="_blank">
              <img src="../assets/linkedin.svg" alt="" />
            </a>
            <p>/victor-dev</p>
          </div>

          <div class="github">
            <a href="https://github.com/VeectorVt" target="_blank">
              <img src="../assets/github.svg" alt="" />
            </a>
            <p>/VeectorVt</p>
          </div>
        </div>
      </div>

      <p class="copy">© 2024 / Victor César / Todos os direitos reservados</p>
    </footer>
  </div>
</template>

<script>
import Swal from "sweetalert2";
import AOS from "aos";
import "aos/dist/aos.css";
import NavbarHome from "../components/NavbarHome.vue";
import SectionHome from "../components/SectionHome.vue";
import SectionAbout from "../components/SectionAbout.vue";
import SectionProjects from "../components/SectionProjects.vue";
import SectionSkills from "../components/SectionSkills.vue";
import { onMounted, toRefs, reactive } from "vue";

export default {
  name: "Home-Page",
  components: {
    NavbarHome,
    SectionHome,
    SectionAbout,
    SectionProjects,
    SectionSkills,
  },

  setup() {
    const data = reactive({
      initialPage: false,
      swalWelcome: true,
    });

    function changeSections() {
      data.initialPage = false;
      data.swalWelcome = false;
    }

    function swalInicial(){
      let timerInterval;
      Swal.fire({
        title:
          "<h1 style=' font-family: Saira, sans-serif;' >Seja bem vindo !</h1>",
        html: "Aguarde, o Portfólio Infinito  &#9854; vai abrir em  <b></b>.",
        timer: 1000,
        timerProgressBar: true,
        allowOutsideClick: false,
        didOpen: () => {
          Swal.showLoading();
          const b = Swal.getHtmlContainer().querySelector("b");
          timerInterval = setInterval(() => {
            b.textContent = Math.trunc(Swal.getTimerLeft() / 1000);
          }, 100);
        },
        willClose: () => {
          clearInterval(timerInterval);
        },
      }).then((result) => {
        /* Read more about handling dismissals below */
        if (result.dismiss === Swal.DismissReason.timer) {
          data.initialPage = true;
          data.swalWelcome = false;
        }
      });
    }

    onMounted(async () => {
     await AOS.init();
     await swalInicial()

    });

    return {
      ...toRefs(data),
      changeSections,
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sections {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  width: 97vw;

  align-items: center;
}
.home-page {
  background-color: #0f0f0f;
  font-family: Saira, sans-serif;
  font-size: 1rem;
  color: #1a3e92;
  overflow-x: hidden;
  z-index: 0;
}

.initialPage {
  /* background: url(../assets/giphy4.gif) center center no-repeat ; */
  font-family: Saira, sans-serif;
  color: #fff;
  width: 100%;
  height: 100vh;
  text-align: center;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  /* background-color: #0f0f0f;
  color: #ffffff; */
  animation-name: changeImage;
  animation-duration: 10s;
  transition: ease-in;
  /* animation-delay: 2s; */
  animation-iteration-count: infinite;
}

.content-initial {
  background-color: #fcfafa;
  padding: 20px;
  color: #000;
  border-radius: 25px;
}

@keyframes changeImage {
  0% {
    background: url(../assets/giphy4.gif) center center no-repeat;
    background-size: cover;
  }
  50% {
    background: url(../assets/giphy3.gif) center center no-repeat;
    background-size: cover;
  }
  75% {
    background: url(../assets/giphy2.gif) center center no-repeat;
    background-size: cover;
  }
  100% {
    background: url(../assets/giphy4.gif) center center no-repeat;
    background-size: cover;
  }
}

footer {
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: #0f0f0f;
  width: 100vw;
  height: 60vh;
}
.contato {
  margin-top: 1em;
  width: 70vw;
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
}
.contato p,
.copy {
  color: #fff;
}

footer h1,
footer h2 {
  text-shadow: #1a3e92 0px 0px 10px;
  margin-top: 1em;
}

.contato a {
  background-color: #1f1f1f;
  border-radius: 5px;
  padding: 10px;
}

.linkedin,
.github {
  display: flex;
  align-items: center;
  flex-direction: row;
  gap: 1em;
}

.github {
  margin-top: 1em;
}
</style>
