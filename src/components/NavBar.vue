<template>
    <nav class="navbar">
        <div class="navbar-menu">
            <ul>
<!-- Se colocó el operador v.bind al atributo href utilizando su mínima expresión el operador : / y se solucinó el enlace a distintas secciones. -->
                <a v-for="nav in navegacion" :key="nav.nombre" :href="nav.enlace" class="nav-item" >{{nav.nombre}}</a>
            </ul>
        </div>
    </nav>
</template>

<script setup>
import { ref } from 'vue';
const navegacion= ref([
    {id:1, nombre:'Educación', enlace:'#educacion'},
    {id:2, nombre:'Experiencia', enlace:'#experiencia'},
    {id:3, nombre:'Proyectos', enlace:'#proyectos'},
    {id:4, nombre:'Habilidades', enlace:'#habilidades'},
]);
</script>

<style scoped>
.navbar {
  background-color:var(--vt-c-indigo); /* Establece el color de fondo usando una variable CSS.*/
  color: #fff; /* Establece el color del texto en blanco. */
  padding: 0.5rem 1rem; /* Añade un padding de 0.5rem arriba y abajo, y de 1rem a los lados. */
  align-items: center; /* Centra verticalmente los elementos dentro de la navbar. */
}

.navbar-item {
  color: #fff; /* Establece el color del texto en blanco. */
  text-decoration: none; /* Elimina el subrayado de los enlaces. */
  margin-right: 1rem; /* Añade un margen derecho de 1rem entre los elementos. */
}

.navbar-menu {
  display: flex; /* Organiza los elementos en línea usando flexbox */
  justify-content: flex-end; 
}

.nav-list {
  list-style: none;
}

a {
  border: 1px solid;
  border-color: hsla(160, 100%, 37%, 0.2);
  border-radius: 5px;
  /* Elimina lo subrayado de los enlaces y elementos con clase "green". */
  text-decoration: none;
  /* Añade una transición suave para los cambios de estilo. */
  transition: 0.4s;
  /* Añade padding alrededor del contenido. */
  padding: 5px;
}

a:hover {
  /* Cambia el color de fondo al pasar el mouse sobre un enlace. */
  background-color: hsla(160, 100%, 37%, 0.2);  
}

@media (max-width: 768px) {
  .navbar-menu {
    display: flex;
    justify-content: flex-end;
    width: 100%;
  }
}
</style>