<template>
  <div>
    <nav class="navbar fixed-top  navbar-expand-lg navbar-dark bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand" href="#"
          >Seja Bem Vindo ao Portfólio "Infinito" &#9854;</a
        >
        <button
          class="navbar-toggler"
          type="button"
          data-bs-toggle="collapse"
          data-bs-target="#navbarNav"
          aria-controls="navbarNav"
          aria-expanded="false"
          aria-label="Toggle navigation"
        >
          <span class="navbar-toggler-icon"></span>
        </button>
        <div
          class="collapse navbar-collapse justify-content-end me-5"
          id="navbarNav"
        >
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#home"
                >Ínicio</a
              >
            </li>
            <li class="nav-item">
              <a class="nav-link" aria-current="page" href="#about"
                >Sobre Mim</a
              >
            </li>

            <li class="nav-item">
              <a class="nav-link" href="#projects">Projetos</a>
            </li>
            <!-- <li class="nav-item">
              <a class="nav-link" aria-current="page" href="#"
                >Experiências</a
              >
            </li> -->
            <li class="nav-item">
              <a class="nav-link" href="#skills">Habilidades</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </div>
</template>

<style>
</style>

<script>
export default {
  name: "NavbarHome",
};
</script>
