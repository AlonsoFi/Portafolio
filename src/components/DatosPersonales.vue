<script setup>
import linkedin from "/src/assets/linkedin_icon.svg";
import instagram from "/src/assets/instagram_icon.svg";
import github from "/src/assets/github_icon.svg";
import cv from "/src/assets/cv_resume_icon.svg";

const title = "Florencia Irupé Alonso";
const descripcion =
  "Estudiante de Tecnicatura Universitaria en Programación - UTN";
const residencia = "Florida, Buenos Aires, Argentina";
const telefono = "3757618767";
const email = "flor.irupe.alonso@gmail.com";
const presentacion =
  "Bienvenidos a mi portafolio profesional de proyectos desarrollados.";
const presentacion2 =
  "Actualmente soy estudiante de la carrera de Tecnicatura Universitaria en Programación, TUP.";
const presentacion3 =
  "Gracias a los conocimientos adquiridos, estoy perfeccionando mis habilidades en desarrollo web y aplicaciones móviles.";
const presentacion4 =
  "Es un placer compartir con ustedes mis avances y proyectos en estas áreas.";

const redesSociales = [
  {
    id: 1,
    name: "linkedin",
    src: linkedin,
    url: "https://www.linkedin.com/in/florencia-irupé-alonso-374a54218/",
  },
  { id: 2, name: "Instagram", src: instagram, url: "" },
  { id: 3, name: "github", src: github, url: "https://github.com/AlonsoFi" },
  { id: 4, name: "curriculum", src: cv, url: "" },
];
</script>

<template>
  <section class="datos-personales">
    <div class="card">
      <h1>{{ title }}</h1>
      <h2>{{ descripcion }}</h2>
      <p>{{ presentacion }}</p>
      <p>{{ presentacion2 }}</p>
      <p>{{ presentacion3 }}</p>
      <p>{{ presentacion4 }}</p>
      <ul class="container-lista">
        <li v-for="red in redesSociales" :key="red.id">
          <a :href="red.url"
            ><img
              class="icon-redsocial"
              :src="red.src"
              width="35rem"
              :alt="red.name"
          /></a>
        </li>
      </ul>
      <h3>Mi teléfono: {{ telefono }}</h3>
      <h4>Mail: {{ email }}</h4>
      <h4>{{ residencia }}</h4>
    </div>
  </section>
</template>

<style scoped>
h1 {
  font-size: 3rem;
  font-weight: 700; /* Negrita para un mayor énfasis */
  color: #4a7c55; /* Verde más fuerte y elegante */
}

h2 {
  font-size: 1.2rem;
  font-weight: 700; /* Negrita para los subtítulos */
  color: #6c8e5d; /* Verde pastel más suave */
}

p {
  font-size: 1rem;
  font-weight: 600;
  margin-bottom: 1rem;
  color: #a4a97f; /* Gris verdoso */
}

.card {
  background-color: #f3f4f1; /* Fondo gris claro */
  border-radius: 10px;
  padding: 10px;
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
  background-color: #4a7c55; /* Verde más fuerte */
  border-radius: 50%;
  padding: 2px;
  margin: 5px;
  box-shadow: 0 0 5px rgba(95, 124, 205, 0.934);
}

.icon-redsocial:hover {
  background-color: #365e44; /* Verde más oscuro para el hover */
  box-shadow: 0 0 5px rgba(251, 249, 249, 0.934);
}

h3,
h4 {
  font-size: 1.2rem;
  font-weight: 600;
  color: #a4a97f; /* Gris verdoso */
}
</style>
