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
    {id:5, nombre:'Intereses', enlace:'#intereses'},
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
  border: 1px solid; /* Añade un borde sólido de 1px. */
  border-color: hsla(160, 100%, 37%, 0.2); /* Define el color del borde usando hsla. */
  border-radius: 5px; /* Redondea las esquinas del borde. */
  text-decoration: none; /* Elimina lo subrayado de los enlaces y elementos con clase "green". */
  transition: 0.4s; /* Añade una transición suave para los cambios de estilo. */
  padding: 5px; /* Añade padding alrededor del contenido. */
}

a:hover {
  background-color: hsla(160, 100%, 37%, 0.2); /* Cambia el color de fondo al pasar el mouse sobre un enlace. */
}

@media (max-width: 768px) {
  .navbar-menu {
    display: flex; /* Organiza los elementos en línea usando flexbox. */
    justify-content: flex-end;  /* Alinea los elementos al final de la navbar. */
    width: 100%; /* Asegura que la navbar ocupe el 100% del ancho en pantallas pequeñas. */
  }
}
</style>