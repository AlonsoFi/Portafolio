<script setup>
import proyecto1 from "/src/assets/annidada-tech.jpeg";
import { ref } from "vue";

var misProyectos = ref([]);
misProyectos.value = [
  {
    id: 1,
    src: proyecto1,
    titulo: "Aplicación de reservas para restaurantes (2024)",
    descripcion:
      "Cree una aplicación móvil con Flutter que permite a los usuarios reservar mesas en restaurantes locales",
    projectoLink: "https://www.google.com.ar",
    githubLink: "https://github.com/usuario/proyecto",
  },
  {
    id: 2,
    src: proyecto1,
    titulo: "Plataforma de E-learning (2024)",
    descripcion:
      "Diseñé y desarrollé una plataforma de educación en línea utilizando Django y React",
    projectoLink: "https://www.google.com.ar",
    githubLink: "https://github.com/usuario/proyecto",
  },
  {
    id: 3,
    src: proyecto1,
    titulo: "Blog Personal con CMS (2024)",
    descripcion:
      "Construí un blog personal con un sistema de gestión (CMS) personalizado en WordPress",
    projectoLink: "https://www.google.com.ar",
    githubLink: "https://github.com/usuario/proyecto",
  },
  {
    id: 4,
    src: proyecto1,
    titulo: "Aplicación de reservas para restaurantes (2024)",
    descripcion:
      "Cree una aplicación móvil con Flutter que permite a los usuarios reservar mesas en restaurantes locales",
    projectoLink: "https://www.google.com.ar",
    githubLink: "https://github.com/usuario/proyecto",
  },
];
</script>

<template>
  <div class="galeria">
    <li class="proyecto" v-for="proyecto in misProyectos" :key="proyecto.id">
      <img :src="proyecto.src" :alt="proyecto.titulo" class="proyecto-imagen" />
      <div class="proyecto-info">
        <h3>{{ proyecto.titulo }}</h3>
        <p>{{ proyecto.descripcion }}</p>
        <div class="proyecto-links">
          <a
            :href="proyecto.projectoLink"
            class="btn-ver-mas"
            target="_blank"
            rel="noopener noreferrer"
            >Ver Proyecto</a
          >
          <a
            :href="proyecto.githubLink"
            class="github-link"
            target="_blank"
            rel="noopener noreferrer"
            >Ver Código en GitHub</a
          >
        </div>
      </div>
    </li>
  </div>
</template>

<style scoped>
/* Contenedor general con fondo verde y bordes redondeados */
.galeria {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  justify-content: center;
  padding: 20px;
  background-color: #e0f7fa; /* Fondo verde suave */
  border-radius: 15px; /* Bordes redondeados */
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1); /* Sombra suave */
}

/* Estilo de cada proyecto */
.proyecto {
  display: flex;
  flex-direction: column;
  max-width: 250px;
  flex: 1 1 300px;
  background-color: #ffffff; /* Fondo blanco para los proyectos */
  border-radius: 12px;
  border: 1px solid #e0e0e0; /* Borde sutil */
  overflow: hidden;
  transition: transform 0.3s, box-shadow 0.3s; /* Efectos de hover */
}

.proyecto:hover {
  transform: translateY(-10px); /* Efecto de elevación */
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.2); /* Sombra más prominente */
}

/* Imagen del proyecto */
.proyecto-imagen {
  width: 100%;
  height: 200px;
  object-fit: cover;
  transition: transform 0.3s ease; /* Efecto de zoom al pasar el mouse */
}

.proyecto-imagen:hover {
  transform: scale(1.05); /* Zoom suave en la imagen */
}

/* Información del proyecto */
.proyecto-info {
  padding: 20px;
  color: #333; /* Color de texto oscuro */
  text-align: center;
}

/* Título del proyecto */
.proyecto-info h3 {
  font-size: 1.5rem;
  font-weight: 600;
  color: #1b5e20; /* Color verde para el título */
  margin: 10px 0;
  letter-spacing: 0.5px;
  text-transform: uppercase; /* Título en mayúsculas */
}

/* Descripción del proyecto */
.proyecto-info p {
  font-size: 1rem;
  color: #757575; /* Descripción en gris claro */
  margin: 10px 0;
  line-height: 1.6;
  font-family: "Roboto", sans-serif; /* Fuente moderna */
}

/* Enlaces del proyecto */
.proyecto-links {
  display: flex;
  flex-direction: column;
  gap: 15px;
  margin-top: 15px;
}

/* Botón de ver más */
.proyecto-links .btn-ver-mas {
  background-color: #388e3c; /* Fondo verde oscuro */
  color: #fff;
  padding: 12px 20px;
  border-radius: 25px; /* Bordes redondeados */
  text-decoration: none;
  font-weight: 500;
  text-transform: uppercase;
  letter-spacing: 1px;
  transition: background-color 0.3s ease; /* Efecto de hover */
}

.proyecto-links .btn-ver-mas:hover {
  background-color: #2c6e26; /* Cambio de color a verde más oscuro al pasar el mouse */
}

/* Estilo del enlace de GitHub */
.proyecto-links .github-link {
  color: #388e3c; /* Color verde */
  text-decoration: none;
  font-size: 1em;
  font-weight: 500;
  transition: color 0.3s ease; /* Efecto de hover */
}

.proyecto-links .github-link:hover {
  color: #1b5e20; /* Cambio a verde más oscuro al pasar el mouse */
  text-decoration: underline;
}
</style>
