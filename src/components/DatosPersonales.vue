<script setup>
import linkedin from '/src/assets/linkedin.webp';
import instagram from '/src/assets/instagram.webp';
import github from '/src/assets/github.png';
import cv from '/src/assets/curriculum.jpg';

const title = 'Gabriel Bruni';
const descripcion = 'Técnico Universitario en Programación - UTN';
const residencia = 'San Rafael, Mendoza, Argentina.';
const presentacion = 'Hola, Bienvenido a mi portafolio de proyectos. Soy desarrollador web con experiencia en aplicaciones web y móviles.';
const redesSociales = [
    {id: 1, name: 'Linkedin', src: linkedin, url: 'https://www.linkedin.com/in/'},
    {id: 2, name: 'Instagram', src: instagram, url: 'https://www.instagram.com/brunigaby?igsh=MW9tYTNucnBpeXNsbA%3D%3D&utm_source=qr'},
    {id: 3, name: 'GitHub', src: github, url: 'https://github.com/GabrielBruni'},
    {id: 4, name: 'Curriculum Vitae', src: cv, url: ''},
];
const telefono = '+54 9 2604 400867';
</script>

<template>
    <section class="datos-personales">
        <div class="card">
            <h1>{{ title }}</h1>
            <h2>{{ descripcion }}</h2>
            <p>{{ presentacion }}</p>
            <ul class="container-lista">
                <li v-for="red in redesSociales" :key="red.id">
                    <a :href="red.url"><img class="icon-redsocial" :src="red.src" width="35rem" :alt="red.name"></a>
                </li>
            </ul>
            <h3>Mi teléfono: {{ telefono }}</h3>
            <h4> {{ residencia }}</h4>
        </div>
    </section>
</template>

<style scoped>
h1 {
    font-size: 2.5rem;
}

p {
    font-size: 1.2rem;
    font-weight: 600;
    margin-bottom: 1rem;
}

.card {
    background-color: rgb(28, 41, 52);
    border-radius: 10px;
    padding: 10px;
    margin: 10px;
    text-align: center;
}

.container-lista {
    display: flex;
    justify-content: center;
    list-style: none;
    padding: 0;
    margin: 0;
    text-align: center;
}

.icon-redsocial {
    align-items: center;
    background-color: aliceblue;
    border-radius: 50%;
    padding: 2px;
    margin: 5px;
    box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
    background-color: rgb(28, 41, 52);
    box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3 {
    font-size: 1.2rem;
    font-weight: 600;
}
</style>