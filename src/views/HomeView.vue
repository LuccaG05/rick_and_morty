<script setup>
import ListPersonagens from '@/components/ListPersonagens.vue';
import { onMounted, reactive, ref } from 'vue';

let personagens = reactive(ref())

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character")
    .then(response => response.json())
    .then(response => {
      personagens.value = response.results
      console.log(personagens)
    })
})
</script>

<template>
  <main>
    <div class="personagens">
      <img src="../../public/personagens.svg" alt="">
    </div>
    <div class="row row-cols-3 mt-4 ">
      <ListPersonagens v-for="personagem in personagens" :key="personagem.id" :name="personagem.name"
        :image="personagem.image" :status="personagem.status" :species="personagem.species" :gender="personagem.gender"
        :location="personagem.location" :episodes="personagem.episode" />
    </div>
  </main>
</template>

<style scoped>
.row {
  display: flex;
  justify-content: center;
  margin: 3rem;
}

.personagens {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100px;
  margin-bottom: 0 !important;
  margin-top: 2rem;
  filter: drop-shadow(rgba(0, 0, 0, 0.24) 0px 3px 8px);
}

.personagens img {
  height: 5rem;
}

@media (max-width: 428px) {
  .personagens img {
    height: 3rem;
  }

  .personagens {
    margin-top: 0;
  }
}
</style>
