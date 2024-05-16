<script setup>
const personagem = defineProps(["name", "image", "status", "species", "gender", "location", "episodes"])

const cor = (status) => {
    if (status === 'Dead'){
        return 'red'
    } else if (status === 'Alive'){
        return '#bfed42'
    }
    return 'black'
} 
</script>

<template>
    <div class="card mb-3 bg-dark" style="width: 500px; padding: 0; margin: 1rem;">
        <div class="row g-0">
            <div class="col-md-5" style=" ">
                <img :src="personagem.image" class="img-fluid rounded-start" alt="...">
            </div>
            <div class="col-md-7">
                <div class="card-body">
                    <h5 class="card-title">{{ personagem.name }}</h5>
                    <hr>
                    <p class="card-text"> <i class="bi bi-circle-fill" :style="{ color: cor(personagem.status) }"></i>Status: {{ personagem.status }}</p>
                    <p class="card-text"> Species: {{ personagem.species }} - {{ personagem.gender }}</p>
                    <p class="card-text"> Location: {{ personagem.location.name }}</p>
                    <p class="card-text"> Episodes: {{ personagem.episodes.length }}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<style>
@import url('https://fonts.googleapis.com/css2?family=Creepster&display=swap');

.card img{
    width: 100%;
}

.card{
    margin: 1.7rem !important;
    border: 6px solid #212529;
    box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;
}

hr{
    color: white;
    margin-top: 0;
}
.card-title{
  display: inline-block;
  font-family: 'Creepster';
  font-size: 1.5rem;
  color: #bfed42;
  margin: 0;
  padding: 0; 
}

.card-title:hover{
    color: white;
}

.bi::before{
    font-size: 0.6rem;
    margin-right: 6px;
}

.card-text{
    align-items: center;
    justify-content: center;
    color: white;
    font-weight: 500;
    margin: 0;
}

@media (max-width: 767px) {
    .card img {
        width: 100%;

    }
}


</style>
