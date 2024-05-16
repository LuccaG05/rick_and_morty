<script setup>

</script>

<template>
  <nav class="navbar navbar-expand-lg bg-dark navbar-dark">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/"><img src="../../public/Rick_and_Morty.svg" alt=""></router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarTogglerDemo02"
        aria-controls="navbarTogglerDemo02" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarTogglerDemo02">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <router-link class="nav-link " aria-current="page" to="/about">Sobre</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

  <router-view />

  <footer class="bg-dark  text-center text-lg-start">
    <div class="text-center p-3">
      UNIMAR - ADS - {{ new Date().getFullYear() }}
    </div>
  </footer>
</template>

<style>
body::-webkit-scrollbar {
  width: 8px;
}

body::-webkit-scrollbar-thumb {
  background-color: #bfed42;
}

body {
  background-color: rgb(126, 126, 126);
}

.navbar {
  font-size: 1.5rem;
  border-bottom: 2px solid #bfed42;
}

.nav-link {
  color: #bfed42;
  font-family: 'Creepster';
  font-size: 3rem;
}

.navbar img {
  height: 6rem;
}

footer {
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  font-weight: 500;
  color: #bfed42;
  border-top: 2px solid #bfed42;

}

@media (max-width: 428px) {
  .navbar img {
    height: 3rem;
  }
}
</style>
