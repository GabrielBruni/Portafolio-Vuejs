<script setup>
import NavBar from './components/NavBar.vue';
import DatosPersonales from './components/DatosPersonales.vue';
import Educación from './components/Educación.vue';
</script>

<template>
  <header>
    <!-- Barra de Navegación -->
    <NavBar />
    <!-- Componentes sobre Datos Personales -->
    <DatosPersonales />
  </header>
  <main>
      <!-- El estilo css de section se encuentra en base.css -->
      <section id="educacion"><h2>Educación - Cursos</h2>
      <Educación />
      </section>
      <section id="experiencia"><h2>Experiencia</h2></section>
      <section id="proyectos"><h2>Proyectos</h2></section>
      <section id="habilidades"><h2>Habilidades</h2></section>
      <section id="intereses"><h2>Intereses</h2></section>
  </main>
</template>

<style scoped>

</style>