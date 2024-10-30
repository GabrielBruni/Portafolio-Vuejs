<script setup>
import { ref } from 'vue';
import FondoLava from './FondoLava.vue';
// Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses.
const intereses = ref([
    'Deporte al aire libre: Disfruto del senderismo como del trail en montaña, siempre salir los fin de semana al campo.',
    'Amante de los motores: También me gusta ir en moto o 4x4 a lugar difíceles de llegar o conocer destinos diferentes a los cuáles no se llega todos los días.',
    'Estudiante de Programación: Actualmente curso en la tecnicatura dentro de la UTN, donde colaboro en grupo para realizar y desarrolar proyectos en conjunto y otros más personales.',
    'Manos a la obra: Tambíen me gusta lo manual como haber estado este año en dos divisiones dentro de una gran empresa, Pampa Energía. Sector uno Servicios Generales y el sector dos Mecánicos. Una experiencia de aprendisaje y experiencia de las mejores sin dudas.'
]);
</script>

<template>
    <div class="intereses-contenedor">
        <FondoLava />
        <ul class="contenedor-lista">
            <li class="item" v-for="interes in intereses" :key="interes">
                {{ interes }}
            </li>
        </ul>
    </div>

    <!-- <div class="intereses-contenedor">
        <ul class="contenedor-lista">
            <li class="item">
                Deporte al aire libre: Disfruto del senderismo como del trail en montaña, siempre salir
                los fin de semana al campo. 
            </li>
            <li class="item">
                Amante de los motores: También me gusta ir en moto o 4x4 a lugar difíceles de llegar o conocer
                destinos diferentes a los cuáles no se llega todos los días. 
            </li>
            <li class="item">
                Estudiante de Programación: Actualmente curso en la tecnicatura dentro de la UTN, donde colaboro
                en grupo para realizar y desarrolar proyectos en conjunto y otros más personales. 
            </li>
            <li class="item">
                Manos a la obra: Tambíen me gusta lo manual como haber estado este año en dos divisiones dentro de una
                gran empresa, Pampa Energía. Sector uno Servicios Generales y el sector dos Mecánicos. Una experiencia
                de aprendisaje y experiencia de las mejores sin dudas.
            </li>
        </ul>
    </div> -->
</template>

<style scoped>
.intereses-contenedor {
    display: flex;
    position: relative;
    margin: 0 auto;
    max-width: 85%;
    padding: 1rem;
}

.contenedor-lista {
    list-style-type: none;
    padding: 1rem;
    margin-bottom: .5rem;
    color: var(--vt-c-white-spft);
    font-size: 1.4rem;
    text-shadow: 3px 3px 6px rgba(0, 0, 0, 1);
}

.item {
    margin-bottom: 1rem;
}
</style>