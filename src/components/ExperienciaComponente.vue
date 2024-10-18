<script setup>
import {ref} from 'vue';
const titulo='Técnico Electromecánico';
const fecha='Desde Marzo 2024 Hasta Septiembre 2024';
const experiencias = ref([
    {id:1, src:'/src/assets/nihuiliv.jpeg', parrafo: 'Técnico Junior en el área de Servicios Generales dentro de la empresa PampaEnergía, en la zona de Valle Grande, exactamente en la central hidroeléctrica Nihuil IV.'},
    {id:2, src:'/src/assets/nihuili.jpeg', parrafo: 'Técnico Junior en el área de Mecánicos dentro de la empresa PampaEnergía, en la zona de El Nihuil, exactamente en las centrales hidroeléctricas Nihuil I y Nihuil II.'},
])
</script>

<template>
    <div class="card">
        <h3 class="titulo">{{ titulo }}</h3>
        <p class="fecha">{{ fecha }}</p>
        <ul class="listado">
            <li class="item" v-for="experiencia in experiencias" :key="experiencia.id">
            <img class="imagen-svg" :src="experiencia.src" width="45rem" :alt="experiencia.parrafo">
            <p>{{ experiencia.parrafo }}</p>
            </li>
        </ul>
    </div>
</template>

<style scoped>
.card{
    display: flex;
    flex-direction: column;
    padding: 2rem;
    background-color: rgb(28, 41, 52);
    border-radius: 15px;
}
/**/
.titulo{
    font-size: 1.5rem;
    color: coral;
}

.fecha{
    font-size: 1rem;
    color: burlywood;
    margin-bottom: 1rem;
}

.listado{
    display: flex;
    flex-direction: column;
}

.item{
    align-items: center;
    display: flex;
    padding: 1rem;
    gap: 1.5rem;
}
</style>