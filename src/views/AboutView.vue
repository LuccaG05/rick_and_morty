<template>
  <div class="about">
    <div class="informacoes">
      <div class="sobre">
        <img src="../../public/sobre.svg" alt="">
      </div>
      <div class="img">
        <img src="../../public/fotoPerfil.jpg" alt="">
      </div>
      <div class="info">
        <h1>Lucca Gonçalves</h1>
        <h1>RA: 1976213</h1>
        <h1>Análise e Desenvolvimento de Sistemas - UNIMAR</h1>
        <h1>3º Termo B</h1>
      </div>
    </div>
  </div>
</template>

<style>
.about {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  text-align: center;
  font-family: 'Creepster';
  color: #212529;
}

.sobre img {
  height: 5rem;
  margin-top: 2rem;
  filter: drop-shadow(rgba(0, 0, 0, 0.24) 0px 3px 8px);
}

.img img {
  filter: drop-shadow(rgba(0, 0, 0, 0.24) 0px 3px 8px);
  width: 100%;
  max-width: 300px;
  aspect-ratio: 1/1;
  object-fit: cover;
  border-radius: 50%;
  object-position: bottom;
  margin: 3rem;
  border: 4px solid #bfed42;
}
</style>
