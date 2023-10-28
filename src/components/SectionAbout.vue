<template>
  <div>
    <!-- Section Home -->
    <section class="sobre-mim">
      <!-- <h3 class="subtitle">Home</h3> -->
      <div class="about-title">
        <img src="../assets/bar.svg">
        <h1>Sobre mim</h1>
        <img src="../assets/bar2.svg">
      </div>
      <div class="about-content">
        <div class="about-text text-center text-wrap">
          <p>
            Sou um desenvolvedor apaixonado pelo que faço e busco sempre
            aprender tecnologias , ferramentas e habilidades que vão me tornar
            um desenvolvedor cada vez mais eficiente e efetivo.Trabalhei com
            projetos envolvendo gestão de cartórios utilizando ferramentas como
            mongoDB , Vue , node e entre outras
          </p>

          <p>
            Atualmente estou estudando Typescript e outras ferramentas do
            ecossistema Vue como Nuxt e cursando Sistemas de Informação
          </p>
        </div>
        <div class="about-image">
          <!-- <img src="" alt=""> -->
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: "SectionAbout",
};
</script>

<style scoped>
/* Sobre mim */
.sobre-mim {
  display: flex;
  align-items: center;
  flex-direction: column;
  background-color: #212529;
  width: 100vw;
  height: 70vh;
}

.about-content {
  display: flex;
  justify-content: space-around;
  flex-direction: row;
  flex-wrap: wrap;
  width: 100vw;
}

.about-title {
  margin-top: 1rem;
  text-align: center;
  display: flex;
  /* -webkit-box-align: center; */
  align-items: center;
  gap: 11px;
  width: 100%;
  /* -webkit-box-pack: center; */
  justify-content: center;
  padding: 3rem 0px;
  color: #fff;
}
.about-image {
  background-image: url(../assets/jslogo.svg);
  background-size: auto ;
  background-repeat: no-repeat;
  animation-name: changeImage;
  animation-duration: 10s;
  transition: linear;
  transition-duration: 0.5s;
  animation-direction: alternate;
  /* animation-delay: 2s; */
  animation-iteration-count: infinite;
  /* 
  height: 40vh;
  margin-top: 1rem; */  
  width: 20vw;
  /* height:10vh; */
}
.about-text {
  /* display: flex;
  justify-content: space-around;
  flex-direction: row;
  flex-wrap: wrap; */
  color: #fff;
  font-size: 1.2rem;
  margin-top: 1rem;
  width: 50vw;
}

@keyframes changeImage {
  0% {
    background: url(../assets/jslogo.svg) center center no-repeat;
    background-size: 200px 200px;
  }
  25% {
    background: url(../assets/node.svg) center center no-repeat;
    background-size: 200px 200px;
  }
  50% {
    background: url("https://www.vectorlogo.zone/logos/mongodb/mongodb-icon.svg") center center no-repeat;
    background-size: 200px 200px;
  }
  75% {
    background: url(../assets/vue.svg) center center no-repeat;
    background-size: 200px 200px;
  }
  85%{
    background: url(../assets/bootstrap-4.svg) center center no-repeat;
    background-size: 200px 200px;
  }
  100% {
    background: url(../assets/jslogo.svg) center center no-repeat;
    background-size: 200px 200px;
  }
}
</style>
