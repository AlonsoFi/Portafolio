<script setup>
import { ref } from "vue";

const fechacolor = ref([]);
fechacolor.value = [
  { color: "#A8D5BA" }, // Verde pastel 1
  { color: "#D1E8E2" }, // Verde pastel 2
  { color: "#B0D9B4" }, // Verde pastel 3
  { color: "#C0D9C5" }, // Verde menta suave
  { color: "#A0C6A8" }, // Verde pastel suave
];

const educacion = ref([]);
educacion.value = [
  {
    fecha: "01/2024 - Actualidad",
    title: "Estudiante de Programación - UTN",
    descripcion:
      "Cursando la carrera de Programación en UTN, enfocándome en desarrollo de software, especialmente en Python y JavaScript, y metodologías ágiles para proyectos escalables.",
    enlace: "https://www.utn.edu.ar",
  },
  {
    fecha: "06/2023 - Actualidad",
    title: "RPA Developer Junior - UiPath",
    descripcion:
      "Desarrolladora Junior en UiPath, creando bots para automatización de procesos y optimización de flujos de trabajo empresariales.",
    enlace: "https://www.uipath.com",
  },
  {
    fecha: "03/2019 - 01/2021",
    title: "Auxiliar Bancario - UCASAL",
    descripcion:
      "Asistí en tareas administrativas y atención al cliente en UCASAL, adquiriendo experiencia en operaciones bancarias y manejo de cuentas.",
    enlace: "https://www.ucasal.edu.ar",
  },
  {
    fecha: "02/2016 - 07/2018",
    title:
      "Técnica Superior en Gestión Contable e Impositiva - Instituto Mariano Pachecoy",
    descripcion:
      "Formación en contabilidad, administración y fiscalidad, complementando mi perfil técnico con habilidades en gestión financiera.",
    enlace: "http://www.pachecoy.edu.ar",
  },
];
</script>

<template>
  <ul>
    <li
      v-for="(item, index) in educacion"
      :key="index"
      :style="{ '--fecha-color': fechacolor[index].color }"
    >
      <div class="fecha">{{ item.fecha }}</div>
      <h3 class="title">{{ item.title }}</h3>
      <div class="descripcion">{{ item.descripcion }}</div>
      <a class="enlace" :href="item.enlace" target="_blank">saber más</a>
    </li>
  </ul>
</template>

<style scoped>
/* Estilos generales */
@import url("https://fonts.googleapis.com/css2?family=Poppins:wght@300;500;700&display=swap");
*,
*::before,
*::after {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

/* Estilo para el cuerpo de la página */
body {
  --color: rgba(30, 30, 30);
  --bgcolor: rgba(245, 245, 245);
  min-height: 100vh;
  display: grid;
  align-content: center;
  gap: 2rem;
  font-family: "Poppins", sans-serif;
  color: var(--color);
  background: var(--bgcolor);
}

/* Estilo para la lista */
ul {
  margin-top: 2rem;
  --col-gap: 2rem;
  --row-gap: 4rem;
  --line-w: 0.25rem;
  display: grid;
  grid-template-columns: 1fr var(--line-w) 1fr; /* Define tres columnas */
  column-gap: var(--col-gap);
  list-style: none;
  width: min(60rem, 90%);
  margin-inline: auto;
  position: relative;
}

/* Estilo para la línea vertical de la línea de tiempo */
ul::before {
  content: "";
  grid-column: 2;
  grid-row: 1 / span 20;
  background: rgb(200, 200, 200);
  width: var(--line-w);
  border-radius: calc(var(--line-w) / 2);
}

/* Estilo para los elementos de la lista con espacio alternado */
ul li:not(:last-child) {
  margin-bottom: var(--row-gap);
}

/* Estilo para cada ítem de la lista */
ul li {
  --inlineP: 1.5rem;
  margin-inline: var(--inlineP);
  display: grid;
  grid-template-rows: min-content min-content min-content;
  position: relative;
}

/* Alineación alternada para los ítems */
ul li:nth-child(odd) {
  grid-column: 1;
  margin-top: 2rem; /* Desfase para los ítems impares */
}

ul li:nth-child(even) {
  grid-column: 3;
  margin-bottom: 2rem; /* Desfase para los ítems pares */
}

/* Estilo para la fecha */
ul li .fecha {
  --dateH: 3rem;
  height: var(--dateH);
  margin-inline: calc(var(--inlineP) * -1);
  text-align: center;
  background-color: var(--fecha-color);
  color: #2c3e50; /* Color oscuro para el texto para asegurar visibilidad */
  font-size: 1.25rem;
  font-weight: 700;
  display: grid;
  place-content: center;
  position: relative;
  border-radius: calc(var(--dateH) / 2) 0 0 calc(var(--dateH) / 2);
}

/* Estilo para el triángulo y el círculo de conexión en elementos impares */
ul li:nth-child(odd) .fecha::before {
  content: "";
  width: var(--inlineP);
  aspect-ratio: 1;
  background: var(--fecha-color);
  background-image: linear-gradient(rgba(0, 0, 0, 0.2) 100%, transparent);
  position: absolute;
  top: 100%;
  clip-path: polygon(0 0, 100% 0, 100% 100%);
  left: 0;
}

ul li:nth-child(odd) .fecha::after {
  content: "";
  position: absolute;
  width: 1rem;
  aspect-ratio: 1;
  background: var(--bgcolor);
  border: 0.3rem solid var(--fecha-color);
  border-radius: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
  left: calc(100% + var(--col-gap) + var(--line-w) / 2);
}

/* Estilos para elementos pares */
ul li:nth-child(even) .fecha {
  border-radius: 0 calc(var(--dateH) / 2) calc(var(--dateH) / 2) 0;
  background-color: var(--fecha-color); /* Color para elementos pares */
}

ul li:nth-child(even) .fecha::before {
  content: "";
  width: var(--inlineP);
  aspect-ratio: 1;
  background: var(--fecha-color);
  background-image: linear-gradient(rgba(0, 0, 0, 0.2) 100%, transparent);
  position: absolute;
  top: 100%;
  clip-path: polygon(0 0, 100% 0, 0 100%);
  right: 0;
}

/* Estilos de título y descripción */
ul li .title,
ul li .descripcion {
  background: var(--bgcolor);
  position: relative;
  padding-inline: 1.5rem;
}

ul li .title {
  overflow: hidden;
  padding-block-start: 1.5rem;
  padding-block-end: 1rem;
  font-size: 1.3rem;
  font-weight: 500;
}

ul li .descripcion {
  padding-block-start: 0.5rem;
  padding-block-end: 1rem;
  font-size: 1rem;
  font-weight: 300;
  line-height: 1.5;
  opacity: 0.7;
  position: relative;
}

ul li .title::after,
ul li .descripcion::after {
  content: "";
  position: absolute;
  width: 90%;
  height: 0.5rem;
  background: #bbb;
  bottom: 0;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 0.3rem;
  opacity: 0.3;
}

/* Estilos para el enlace */
ul li .enlace {
  text-decoration: none;
  font-weight: 500;
  font-size: 1rem;
  color: #2c3e50; /* Aseguramos que el texto sea legible */
  transition: 0.2s ease-out;
}

ul li .enlace:hover {
  color: #1e76d1; /* Color para cuando se pasa el ratón */
}
</style>
