<template>
  <nav class="navbar">
    <div class="navbar-menu">
      <ul class="nav-list">
        <!-- Agregar el enlace de "Inicio" primero -->
        <li class="nav-item-wrapper">
          <a href="#top" class="nav-item">Inicio</a>
        </li>

        <!-- Los enlaces de navegación -->
        <li
          v-for="nav in navegacion"
          :key="nav.nombre"
          class="nav-item-wrapper"
        >
          <a :href="nav.enlace" class="nav-item">
            {{ nav.nombre }}
          </a>
        </li>
      </ul>
    </div>
  </nav>
</template>

<script setup>
import { ref } from "vue";

/* Arreglo de objetos para la navegación */
const navegacion = ref([
  { id: 1, nombre: "Educación", enlace: "#educacion" },
  { id: 2, nombre: "Experiencia", enlace: "#experiencia" },
  { id: 3, nombre: "Proyectos", enlace: "#proyectos" },
  { id: 4, nombre: "Habilidades", enlace: "#habilidades" },
  { id: 5, nombre: "Intereses", enlace: "#intereses" },
]);
</script>

<style scoped>
/* Estilos de la barra de navegación */
.navbar {
  background-color: #4a7c55;
  color: #f3f4f1;
  padding: 0.2rem 1rem;
  align-items: center;
  border-radius: 8px;
  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  z-index: 1000;
}

.navbar-menu {
  display: flex;
  justify-content: center;
  width: 100%;
}

.nav-list {
  display: flex;
  justify-content: center;
  gap: 10px; /* Separación entre botones */
  list-style: none;
  padding: 0;
  margin: 0;
  width: 100%;
}

/* Contenedor para cada enlace */
.nav-item-wrapper {
  flex: 1; /* Ocupa el mismo espacio para cada enlace */
}

/* Estilos para los elementos del menú */
.nav-item {
  color: #f3f4f1;
  text-decoration: none;
  display: block;
  padding: 10px 0;
  border: 1px solid #365e44;
  border-radius: 5px;
  text-align: center;
  transition: 0.4s;
  width: 100%; /* Asegura que cada botón ocupe todo el ancho de su contenedor */
}

/* Cambiar el color de fondo al pasar el mouse */
.nav-item:hover {
  background-color: #365e44;
  color: #ffffff;
}

@media (max-width: 768px) {
  .nav-list {
    flex-direction: column;
  }
}
</style>
