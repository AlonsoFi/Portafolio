<script setup>
import { ref } from "vue";
import FondoLava from "./FondoLava.vue";

// Este es un arreglo con ref para que se pueda reactivar el cambio de los intereses
const intereses = ref([
  "Gestión y Optimización de Procesos Financieros: Me interesa encontrar nuevas formas de mejorar la eficiencia en los procesos contables y bancarios, buscando siempre una mayor precisión y reducción de tiempos.",
  "Análisis de Datos Financieros y Contables: Apasionada por el análisis de datos, disfruto buscando patrones y tendencias que ayuden a tomar decisiones más informadas y a mejorar la gestión económica de las empresas.",
  "Estrategias Impositivas y Legales: Mi interés está en explorar y aplicar estrategias fiscales que favorezcan la correcta presentación y liquidación de impuestos, buscando siempre la conformidad con la legislación vigente.",
  "Automatización de Tareas Administrativas: Con mi experiencia en RPA, me interesa optimizar tareas repetitivas y manuales dentro de los procesos administrativos, lo que mejora la eficiencia y la precisión en los resultados.",
]);
</script>

<template>
  <div class="intereses-contenedor">
    <!-- Fondo de lava mantiene la animación de fondo -->
    <FondoLava />
    <ul class="contenedor-lista">
      <li class="item" v-for="interes in intereses" :key="interes">
        {{ interes }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
/* Estilo para el contenedor principal */
.intereses-contenedor {
  display: flex;
  position: relative;
  margin: 0 auto;
  max-width: 85%;
  padding: 1rem;
  background-color: rgba(
    145,
    198,
    167,
    0.8
  ); /* Fondo verde suave y semi-transparente */
  border-radius: 8px; /* Bordes redondeados para suavizar el diseño */
  z-index: 1; /* Para asegurarse de que la lista de intereses esté por encima del fondo de lava */
}

/* Estilo para la lista de intereses */
.contenedor-lista {
  list-style-type: none;
  padding: 1rem;
  margin-bottom: 0.5rem;
  color: #1e1e1e; /* Color de texto más oscuro para mejorar la legibilidad */
  font-size: 1.6rem; /* Aumentar el tamaño de la fuente */
  font-weight: 500; /* Peso de fuente medio para mejor legibilidad */
  z-index: 2; /* Para asegurarse de que el texto esté por encima del fondo de lava */
}

/* Estilo para cada ítem de la lista */
.item {
  margin-bottom: 1rem;
  line-height: 1.8; /* Espaciado para mejorar la legibilidad */
  text-align: left; /* Alineación a la izquierda para mayor claridad */
  text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.2); /* Sombra más pronunciada para destacar el texto */
}

/* Sombra sutil en el texto para mayor contraste */
.contenedor-lista li {
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.25); /* Sombra adicional para destacar más */
}
</style>
