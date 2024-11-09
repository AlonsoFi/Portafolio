<script setup>
import NavBar from "./components/NavBar.vue";
import DatosPersonales from "./components/DatosPersonales.vue";
import Educacion from "./components/EducacionComponente.vue";
import ExperienciaComponente from "./components/ExperienciaComponente.vue";
import ProyectosComponente from "./components/ProyectosComponente.vue";
import HabilidadesComponente from "./components/HabilidadesComponente.vue";
import InteresesComponente from "./components/InteresesComponente.vue";
</script>

<template>
  <header id="top">
    <!-- Barra de Navegación -->
    <NavBar />
    <!-- Componente Datos Personales -->
    <DatosPersonales />
  </header>

  <main>
    <!-- Estilo CSS de section se encuentra en base.css -->
    <section id="educacion">
      <h2>Educación - Cursos</h2>
      <Educacion />
    </section>
    <section id="experiencia">
      <h2>Experiencia</h2>
      <ExperienciaComponente />
    </section>
    <section id="proyectos">
      <h2>Proyectos</h2>
      <ProyectosComponente />
    </section>
    <section id="habilidades">
      <h2>Habilidades</h2>
      <HabilidadesComponente />
    </section>
    <section id="intereses">
      <h2>Intereses</h2>
      <InteresesComponente />
    </section>
  </main>

  <footer>
    <!-- Enlace "Inicio" para volver al principio de la página -->
    <a href="#top">Inicio</a>
    <p>© 2024 Alonso Florencia - Portafolio web - tutorial UTN FRSR</p>
  </footer>
</template>

<!-- Estilos -->
<style scoped>
footer {
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
  font-size: 1.3rem;
  background-color: rgba(145, 198, 167, 0.8); /* Fondo verde suave */
}

h2 {
  font-size: 2rem;
  font-weight: 700; /* Negrita en los títulos */
  color: #91c6a7; /* Verde suave para los títulos */
}

footer a {
  color: #91c6a7; /* Verde para los enlaces */
  text-decoration: none;
  margin-bottom: 1rem; /* Añadir espacio debajo del enlace "Inicio" */
}

footer p {
  color: #1e1e1e; /* Color oscuro para mejorar la legibilidad */
}
</style>
