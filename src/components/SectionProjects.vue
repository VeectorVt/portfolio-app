<template>
  <div>
    <!-- Section Home -->
    <section class="projetos">
      <!-- <h3 class="subtitle">Home</h3> -->
      <div class="project-title">
        <img class="mt-5" src="../assets/bar.svg" alt="" />
        <h1 class="title mt-5">Projetos</h1>
        <img class="mt-5" src="../assets/bar2.svg" alt="" />
      </div>

      <div data-aos-delay="500" data-aos-once="true" data-aos="flip-up" data-aos-duration="2000" class="projetos-carrossel carousel slide" id="carousel">
        <!-- data-bs-ride="true" -->
        <div>
          <div class="carousel-inner">
            <div class="carousel-item active">
              <!-- Rick and Morty -->

              <div
                @click="altContent('rickMorty', true)"
                class="carousel-item-div"
                id="rick-content"
              >
                <img
                  src="../assets/rick-morty-app.png"
                  class="d-block w-80 img-rick"
                />
                <div class="carousel-item-div-text">
                  <h3 style="color: #00b0c8">Rick and Morty App</h3>
                  <span
                    >Aplicação criada com base na famosa api do rick-morty ,
                    buscando todos os personagens por status , Raça e nome
                  </span>
                </div>
              </div>
            </div>

            <!-- Pokedex -->

            <div class="carousel-item">
              <div
                class="carousel-item-div"
                @click="altContent('pokeDex', false)"
              >
                <img src="../assets/pokedex.png" class="d-block w-80" />
                <div class="carousel-item-div-text">
                  <h3 style="color: #00b0c8">Pokedex</h3>
                  <span
                    >Aplicação criada com base na API pública da pokedex
                
                  </span>
                </div>
              </div>
            </div>

            <!--  -->

            <div class="carousel-item">
              <div
                class="carousel-item-div"
                @click="altContent('dogCat', false)"
              >
                <img src="../assets/dog-cat.png" class="d-block w-80" />
                <div class="carousel-item-div-text">
                  <h3 style="color: #00b0c8">Dog-Cat-Mimo</h3>
                  <span
                    >Landing page criada para um infoproduto , relacionado a
                    saúde de cães e gatos
                  </span>
                </div>
              </div>
            </div>

            <div class="carousel-item">
              <div class="carousel-item-div" @click="altContent('codar', true)">
                <img class="codar-img" src="../assets/codar.png" />
                <div class="carousel-item-div-text">
                  <h3 style="color: #00b0c8">Codar (Landing Page)</h3>
                  <span
                    >Landing page criada para página de venda de sites!
                  </span>
                </div>
              </div>
            </div>
          </div>
          <button
            class="carousel-control-prev"
            type="button"
            data-bs-target="#carousel"
            data-bs-slide="prev"
          >
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
          </button>
          <button
            class="carousel-control-next"
            type="button"
            data-bs-target="#carousel"
            data-bs-slide="next"
          >
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
          </button>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import { onMounted, toRefs, reactive } from "vue";
import * as bootstrap  from "bootstrap";
import Swal from "sweetalert2";
export default {
  name: "SectionProjects",

  setup() {
    function startSlide() {
      const myCarouselElement = document.querySelector("#carousel");

      const carousel = new bootstrap.Carousel(myCarouselElement, {
        interval: 1000,
        touch: false,
      });

      return carousel;
    }

    const methods = reactive({
      altContent(project, inAir) {
        Swal.fire({
          html: inAir
            ? "<h3 style=' font-family: Saira, sans-serif;'>Deseja ir para o Repositório ou Aplicação no ar ?</h3>"
            : "<h3 style=' font-family: Saira, sans-serif;' >Deseja ir para o Repositório ?</h3>",
          showConfirmButton: inAir ? true : false,
          showDenyButton: true,
          showCancelButton: true,
          confirmButtonText: "Aplicação no ar",
          denyButtonText: `Repositório`,
          denyButtonColor: "#132141",
          width: 600,

          padding: "3em",
          color: "#000",
          background: "#fff",
        }).then((result) => {
          if (result.isConfirmed) {
            switch (project) {
              case "rickMorty":
                window.open(
                  "https://64dacc12cb9ad60a84bf90d9--warm-pavlova-bd9a45.netlify.app/",
                  "_blank"
                );
                break;
              case "codar":
                window.open(
                  "https://veectorvt.github.io/codar/codar.html",
                  "_blank"
                );
                break;
              default:
                break;
            }
          } else if (result.isDenied) {
            switch (project) {
              case "rickMorty":
                window.open(
                  "https://github.com/VeectorVt/rick-and-morrty-app",
                  "_blank"
                );
                break;
              case "codar":
                window.open("https://github.com/VeectorVt/codar", "_blank");

                break;

              case "pokeDex":
                window.open("https://github.com/VeectorVt/pokedex", "_blank");
                break;

              case "dogCat":
                window.open(
                  "https://github.com/VeectorVt/landing-page-dog-cat",
                  "_blank"
                );
                break;
              default:
                break;
            }
          }
        });
      },

      // altContentOff() {
      //   const rickMortyDiv = document.querySelector(".rick-morty-alt");
      //   const rickContent = document.querySelector("#rick-content");
      //   rickMortyDiv.style.display = "none";
      //   rickContent.style.display = "flex";
      //   // rickMortyDiv.style.display = "flex";
      // },
    });

    onMounted(async () => {
      startSlide;
    });

    return {
      ...toRefs(methods),
    };
  },
};
</script>

<style scoped>
.projetos {
  display: flex;
  align-items: center;
  flex-direction: column;
  /* background-color: rgb(152, 28, 209); */
  width: 100vw;
  height: 100vh;
  scroll-behavior: smooth;
}
.project-title{
  display: flex;
  gap: 10px;
  color: #fff;
  /* justify-content: space-around; */
  flex-direction: row;
  /* flex-wrap: wrap; */
}
.projetos-carrossel {
  width: 50vw;
  /* height: 50vh; */
  background-color: rgb(11, 11, 11);
  position: relative;
  cursor: grab;
  padding: 3rem;
  margin-top: 2rem;

  display: flex;
  -webkit-box-pack: center;
  justify-content: center;
  -webkit-box-align: center;
  align-items: center;
  box-shadow: #00ad6f 0px 0px 10px;
  flex-direction: column;
}

.carousel-item-div-text {
  color: #fff;
  font-size: 1rem;
  margin-top: 3rem;
  width: 20vw;
}

.carousel-item-div-text h3 {
  text-decoration: underline;
  cursor: pointer;
}
.carousel-item-div {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  z-index: 0;
}

.carousel-item-div img {
  height: 30vh;
  border-radius: 10px;
  /* box-shadow: #9fa8bd 0px 0px 10px; */
}

.codar-img{
  width: 30vw;
}.rick-morty-alt {
  display: none;
  justify-content: center;
  flex-direction: column;
  align-items: center;
}
/* .rick-morty-hover:hover{
  display: flex;
  z-index: 1;
} */

/* .projetos-carrossel::after {
  background: linear-gradient(
    235deg,
    rgb(0, 173, 111),
    rgb(0, 173, 111),
    rgb(0, 173, 111)
  );

  z-index: -2;
  filter: blur(5px);
} */
</style>
