<template>
  <div>
    <!-- Section Home -->
    <section id="home" class="home">
      <!-- <div class=""> -->
      <!-- <div class="home-content"> -->
      <div class="home-content">
        <div>
          <h3 class="subtitle">Oi eu sou ,</h3>
          <h1 class="title-home">Victor César</h1>
          <h3 class="subtitle-home">Desenvolvedor Web</h3>

          <div class="social-media">
            <a href="https://www.linkedin.com/in/victor-cesar-dev/" target="_blank">
              <div class="linkedin">
              
                <img src="../assets/linkedin.svg" alt="">
              </div>
            </a>

           <a href="https://github.com/VeectorVt" target="_blank">
            <div class="github">
              <GithubSvg/>
              <!-- <img src="../assets/github.svg" alt=""> -->
            </div>
           </a>
            
          </div>
        </div>
        <!-- </div> -->
        <div class="image-home"></div>
      </div>
      <!-- </div> -->
    </section>
  </div>
</template>

<script>
import GithubSvg from '../components/includes/github-svg.vue'
export default{
  name:'SectionHome',

  components:{
    GithubSvg
  }
};

</script>

<style scoped>

/* HOME */

.home {
  display: flex;
  align-items: center;
  flex-direction: column;
  /* justify-content: space-around; */

  margin-top: 5rem;
  width: 100vw;
  height: 80vh;
}


.home-content {
  display: flex;
  justify-content: space-around;
  flex-direction: row;
  flex-wrap: wrap;

  width: 70vw;
}

.title-home{
  /* font-family: monospace; */
  font-size: 5rem;
}


.subtitle-home {
  font-size: 2rem;
  font-family: monospace;
  border-right: 4px solid #fff;
  text-shadow: #1a3e92 0px 0px 10px;
  width: 19ch;
  white-space: nowrap;
  overflow: hidden;
  animation: typing 2s steps(19), blinking 0.5s infinite step-end alternate;
}

.image-home {
  background-image: url(../assets/foto-perfil.png);
  background-size: cover;
  /* object-fit: contain; */
  background-repeat: no-repeat;
  width: 20vw;
  height: 50vh;
  border-radius: 50%;
  box-shadow: #9fa8bd 0px 0px 10px;
  position: relative;
  animation: imageMove 2.1s linear 0s infinite alternate-reverse none running;
}

@keyframes imageMove {
  0% {
    top: 15px;
  }
  100% {
    top: -15px;
  }
}

@keyframes typing {
  from {
    width: 0;
  }
}

@keyframes blinking {
  50% {
    border-color: transparent;
  }
}

.social-media {
  margin-top: 1em;
  display: flex;
  gap: 1em;
  flex-direction: row;
}
.social-media a{
  background-color: #1F1F1F;
  border-radius: 5px;
  padding: 10px;
}






</style>


