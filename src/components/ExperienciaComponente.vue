<script setup>
import icono1 from "/src/assets/crab-svgrepo-com.svg";
import icono2 from "/src/assets/crocodile-svgrepo-com.svg";
import icono3 from "/src/assets/dinosaur-svgrepo-com.svg";
import icono4 from "/src/assets/elk-svgrepo-com.svg";
import icono5 from "/src/assets/jellyfish-svgrepo-com.svg";

import { ref } from "vue";
const titulo = "Experiencia Profesional";
const fecha = "Desde 2017 - Actualidad";
const experiencias = ref([
  {
    id: 1,
    src: icono1,
    parrafo:
      "Administración Contable | División Industrial SA (11/2023 - Actualidad): Supervisión y registro de transacciones comerciales para garantizar la exactitud y la integridad de los datos financieros.",
  },
  {
    id: 2,
    src: icono2,
    parrafo:
      "Desarrolladora Junior en RPA | Estudio Carnicero (06/2023 - 09/2023): Creación de secuencias para el LogIn y LogOut en el sistema de AFIP.",
  },
  {
    id: 3,
    src: icono3,
    parrafo:
      "Administrativa | Comercial De Turismo S.A (01/2020 - 03/2023): Utilización de Excel para la gestión y análisis de datos financieros y operativos.",
  },
  {
    id: 4,
    src: icono4,
    parrafo:
      "Cajera / Tesorera | Nordic SRL (07/2019 - 01/2020): Responsable del manejo preciso y seguro de transacciones en efectivo.",
  },
  {
    id: 5,
    src: icono5,
    parrafo:
      "Vendedora | La Aripuca (09/2017 - 11/2018): Trabajo activo para alcanzar y superar los objetivos de ventas establecidos por la empresa.",
  },
]);
</script>

<template>
  <div class="card">
    <h3 class="titulo">{{ titulo }}</h3>
    <p class="fecha">{{ fecha }}</p>
    <ul class="listado">
      <li
        class="item"
        v-for="experiencia in experiencias"
        :key="experiencia.id"
      >
        <img
          class="imagen-svg"
          :src="experiencia.src"
          width="45rem"
          :alt="experiencia.parrafo"
        />
        <p>{{ experiencia.parrafo }}</p>
      </li>
    </ul>
  </div>
</template>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  padding: 2rem;
  background-color: #4a7c55; /* Verde de fondo */
  border-radius: 15px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.15); /* Sombra más sutil */
  transition: 0.3s all ease; /* Suaviza las transiciones */
}

.card:hover {
  transform: translateY(-5px); /* Efecto hover para darle un toque dinámico */
}

.titulo {
  font-size: 2rem; /* Tamaño de fuente mayor para mayor impacto */
  color: #f3f4f1; /* Texto claro */
  font-family: "Poppins", sans-serif; /* Tipografía moderna */
  font-weight: 600; /* Negrita para mayor énfasis */
  margin-bottom: 0.5rem;
  letter-spacing: 1px; /* Espaciado entre letras para un toque más sofisticado */
  text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.2); /* Sombra para el título */
}

.fecha {
  font-size: 1.2rem;
  color: #e0e3e0; /* Color más suave para la fecha */
  margin-bottom: 1rem;
  font-family: "Roboto", sans-serif; /* Fuente más ligera y moderna */
  font-weight: 500;
}

.listado {
  display: flex;
  flex-direction: column;
  gap: 1.2rem;
}

.item {
  display: flex;
  align-items: center;
  gap: 1.5rem;
  padding: 1.2rem;
  background-color: #365e44; /* Fondo más oscuro */
  border-radius: 10px;
  color: #f3f4f1; /* Texto claro */
  transition: 0.3s all ease; /* Transición suave al hacer hover */
}

.item:hover {
  background-color: #4a7c55; /* Efecto hover para cambiar el fondo */
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2); /* Sombra suave al hacer hover */
}

.imagen-svg {
  width: 55px;
  height: 55px;
  transition: 0.3s all ease;
}

.imagen-svg:hover {
  transform: rotate(
    15deg
  ); /* Rotación ligera al pasar el mouse sobre el icono */
}

p {
  font-size: 1rem;
  font-family: "Roboto", sans-serif;
  color: #e1e1e1;
  line-height: 1.6;
  letter-spacing: 0.5px;
}

p:hover {
  color: #f3f4f1; /* Cambiar color al pasar el mouse sobre el texto */
}
</style>
