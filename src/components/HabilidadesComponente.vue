<script setup>
// Se importa ref de vue para poder usarlo.
import { ref } from 'vue';
// Se crea un array de objetos con las habilidades.
// Este es un array de objetos con habilidades que se pueden modificar o agregar.
const habilidades = ref([
    {// Se crea un objeto con id, nombre y habilidades.
        id: 1, nombre: 'Lenguajes de Programación', habilidades: [
            // Se crea un objeto con id, nombre, nivel e ícono.
            { id: 1, nombre: 'JavaScript', nivel: 'Principiante', icono: '/src/components/icons/JavaScript.svg'},
            { id: 2, nombre: 'Python', nivel: 'Principiante', icono: '/src/components/icons/Python.svg'},
            { id: 3, nombre: 'HTML / CSS', nivel: 'Principiante', icono: '/src/components/icons/HTML.svg'},
            { id: 4, nombre: 'Java', nivel: 'Principiante', icono: '/src/components/icons/Java.svg'},
            { id: 5, nombre: 'SQL', nivel: 'Principiante', icono: '/src/components/icons/SQL.svg'},
        ]
    },
    {
        id: 2, nombre: 'Frameworks y Librerías', habilidades: [
            { id: 1, nombre: 'React.js', nivel: 'Principiante', icono: '/src/components/icons/Reacts.svg'},
            { id: 2, nombre: 'Vue.js', nivel: 'Principiante', icono: '/src/components/icons/Vue.svg'},
            { id: 3, nombre: 'Node.js', nivel: 'Principiante', icono: '/src/components/icons/Node.svg'},
            { id: 4, nombre: 'DJango', nivel: 'Principiante', icono: '/src/components/icons/DJango.svg'},
            { id: 5, nombre: 'Bootstrap', nivel: 'Principiante', icono: '/src/components/icons/Bootstrap.svg'},
        ]
    },
    {
        id: 3, nombre: 'Herramientas y Sofware', habilidades: [
            { id: 1, nombre: 'Git', nivel: 'Principiante', icono: '/src/components/icons/Git.svg' },
            { id: 2, nombre: 'Docker', nivel: 'Principiante', icono: '/src/components/icons/Docker.svg' },
            { id: 3, nombre: 'Cypress', nivel: 'Principiante', icono: '/src/components/icons/Cypress.svg' },
            { id: 4, nombre: 'Figma', nivel: 'Principiante', icono: '/src/components/icons/Figma.svg' },
            { id: 5, nombre: 'Visual Studio Code', nivel: 'Principiante', icono: '/src/components/icons/VSC.svg' },
        ]
    },
    {
        id: 4, nombre: 'Base de Datos', habilidades: [
            { id: 1, nombre: 'MongoDB' , nivel: 'Principiante', icono: '/src/components/icons/MongoDB.svg' },
            { id: 2, nombre: 'MySQL' , nivel: 'Principiante', icono: '/src/components/icons/MySQL.svg' },
            { id: 3, nombre: 'PostgreSQL' , nivel: 'Principiante', icono: '/src/components/icons/PostgreSQL.svg' },
        ]
    },
    {
        id: 5, nombre: 'Idiomas', habilidades: [
            { id: 1, nombre: 'Español', nivel: 'Nativo', icono: '/src/components/icons/Argentina.svg' },
            { id: 2, nombre: 'Inglés', nivel: 'Principiante', icono: '/src/components/icons/EEUU.svg' },
            { id: 3, nombre: 'Italiano', nivel: 'Principiante', icono: '/src/components/icons/Italia.svg' },
        ]
    }
]);
</script>

<template>
    <!-- Este componente vue funciona de esta forma: -->
    <div class="skills-contenedor">
        <!-- Se reconoce el array habilidades con v-fory se asigna la key habilidad.id: -->
        <div v-for="habilidad in habilidades" :key="habilidad.id" class="skills-categoria">
            <!-- Se muestra el nombre de la habilidad: -->
            <h3>{{ habilidad.nombre }}</h3>
            <ul class="skills">
                <!-- Se reconoce el array habilidades con v-for y se asigna la key habilidad.id: -->
                <li v-for="habilidad in habilidad.habilidades" :key="habilidad.id" class="skill">
                    <!-- Se muestra el ícono de la habilidad y el nombre de la habilidad con su nivel: -->
                    <img :src="habilidad.icono" :alt="habilidad.nombre">
                    <!-- Se muestra el ícono de la habilidad y el nombre de la habilidad con su nivel: -->
                    <span>{{ habilidad.nombre }}: {{ habilidad.nivel }}</span>
                </li>
            </ul>
        </div>
    </div>


<!-- <style scoped>
.skills-contenedor {
    padding: 2rem;
    /* Fondo cargado desde una imagen estática en Assets. */
    /*background-image: url();*/
    /*background-size: cover;*/
    /*background-position: center;*/
    /*background-repeat: no-repeat;*/
    /* Fondo con gradiente. */
    /*background: linear-gradient(-45deg, #021526, #03346E, #6EACDA, #E2E2B2);*/
    /* Fondo color sólido. */
    background-color: rgb(28, 41, 52);
}

/* .skills-categoria {
    margin-bottom: 20px;
}

.skills-categoria h3 {
    display: flex;
    justify-content: left;
    margin-bottom: 10px;
    font-size: 1.5rem;
    color: aliceblue;
    font-size: 1.5rem;
    font-weight: bold;
}

.skills {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}

.skill {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    background-color: rgba(241, 245, 243, 0.856);
    padding: 0.3rem;
    border-radius: 8px;
    box-shadow: 0px 4px 12px rgba(2, 151, 151, 0.963);
    flex: 1 1 200px;
    max-width: 250px;
}

.skill:hover {
    background-color: rgba(2, 151, 151, 0.963);
}

.skill img {
    width: 35px;
    height: 35px;
}

.skill span {
    font-size: 1.3rem;
    color: #333;
}

.skill:hover {
    font-size: 1.3rem;
    transition: 2s ease;
}

@media (max-width: 768px) {
    .skills-categoria h3 {
        justify-content: center;
    }

    .skill {
        justify-content: center;
    }
}
</style> */ -->
</template>

<style scoped>
.skills-contenedor {
    padding: 2rem;
    /*Fondo cargado desde una imagen estatica en Assets*/
    /* background-image: url('/src/assets/fondo-proyectos.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat; */
    /*Fondo con gradiente*/
    background: linear-gradient(-45deg, #021526, #03346E, #6EACDA, #E2E2B6);
    /*Fondo con color solido*/
    /* background-color: rgb(28, 41, 52); */
}

.skills-categoria {
    margin-bottom: 20px;
}

.skills-categoria h3 {
    display: flex;
    justify-content: left;
    margin-bottom: 10px;
    font-size: 1.5em;
    color: aliceblue;
    font-size: 1.5em;
    font-weight: bold;
}

.skills {
    display: flex;
    justify-content: space-evenly;
    flex-wrap: wrap;
    gap: 20px;
}

.skill {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 10px;
    background-color: rgba(241, 245, 243, 0.856);
    padding: 0.3em;
    border-radius: 8px;
    box-shadow: 0px 4px 12px rgba(2, 151, 151, 0.963);
    flex: 1 1 200px;
    max-width: 250px;
}

.skill:hover {
    background-color: rgba(2, 151, 151, 0.963);
}

.skill img {
    width: 35px;
    height: 35px;
}

.skill span {
    font-size: 1em;
    color: #333;
}

.skill:hover {
    font-size: 1.3em;
    transition: 2s ease;
}

@media (max-width: 768px) {
    .skills-categoria h3 {
        justify-content: center;
    }

    .skill {
        justify-content: center;
    }
}
</style>