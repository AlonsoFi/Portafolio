<template>
  <svg preserveAspectRatio="xMidYMid slice" viewBox="10 10 80 80">
    <defs></defs>
    <!-- Elipses suaves con bordes delicados -->
    <ellipse
      fill="none"
      stroke="#A1C6A7"
      stroke-width="0.5"
      class="bubble bubble-1"
      cx="20"
      cy="20"
      rx="15"
      ry="10"
    />
    <ellipse
      fill="none"
      stroke="#A7D1A4"
      stroke-width="0.5"
      class="bubble bubble-2"
      cx="40"
      cy="40"
      rx="12"
      ry="8"
    />
    <ellipse
      fill="none"
      stroke="#7DBF9E"
      stroke-width="0.5"
      class="bubble bubble-3"
      cx="60"
      cy="60"
      rx="14"
      ry="9"
    />
    <ellipse
      fill="none"
      stroke="#6F9F89"
      stroke-width="0.5"
      class="bubble bubble-4"
      cx="80"
      cy="80"
      rx="16"
      ry="11"
    />
    <ellipse
      fill="none"
      stroke="#55A28C"
      stroke-width="0.5"
      class="bubble bubble-5"
      cx="50"
      cy="30"
      rx="18"
      ry="12"
    />
    <ellipse
      fill="none"
      stroke="#9ABF9A"
      stroke-width="0.5"
      class="bubble bubble-6"
      cx="30"
      cy="70"
      rx="15"
      ry="10"
    />
  </svg>
</template>

<style scoped>
/* Animación de flotación para las burbujas */
@keyframes float {
  0% {
    transform: translateY(0) scale(1);
  }
  50% {
    transform: translateY(-15px) scale(1.05);
  }
  100% {
    transform: translateY(0) scale(1);
  }
}

/* Animaciones alternadas para cada burbuja */
.bubble-1 {
  animation: float 6s ease-in-out infinite;
}
.bubble-2 {
  animation: float 8s ease-in-out infinite;
}
.bubble-3 {
  animation: float 5s ease-in-out infinite;
}
.bubble-4 {
  animation: float 7s ease-in-out infinite;
}
.bubble-5 {
  animation: float 9s ease-in-out infinite;
}
.bubble-6 {
  animation: float 6.5s ease-in-out infinite;
}

/* Ajustes generales del SVG */
svg {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 95%;
  z-index: -1;
  border-radius: 8px;
  background-color: #f7f0f7; /* Fondo suave y cálido */
}

/* Estilo general de la página */
body {
  font-family: "Arial", sans-serif;
  background-color: #f7f0f7; /* Fondo general suave */
  margin: 0;
  padding: 0;
  color: #333; /* Texto en color oscuro para mejorar la legibilidad */
}

/* Para el contenedor del texto */
.text-container {
  z-index: 10;
  position: relative;
  color: #333; /* Color oscuro para el texto */
  font-size: 1.5rem;
  line-height: 1.6;
  font-weight: 400;
  text-align: center;
  padding: 2rem;
}

/* Sombra para el texto (opcional) */
.text-container h1,
.text-container p {
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3); /* Sombra suave */
}
</style>
