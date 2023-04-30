<template>
  <nav class="navbar navbar-expand-lg navbar-light bg-primary">
    <div class="container">
      <a class="navbar-brand text-white" href="./">
        <img src="/favicon-32x32.png" alt="padrinos sin limites" />
      </a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item">
            <NuxtLink class="nav-link text-white" aria-current="page" to="/"
              >INICIO</NuxtLink
            >
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link text-white" to="/about"
              >QUIÉNES SOMOS</NuxtLink
            >
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link text-white" to="/team">EQUIPO</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link text-white" to="/faq">PREGUNTAS</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link text-white" to="/voces">VOCES</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link text-white" to="/materials"
              >MATERIALES</NuxtLink
            >
          </li>

          <li class="nav-item">
            <a
              class="nav-link text-white"
              href="mailto: ruralgodparents@gmail.com"
              >CONTACTO</a
            >
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>

<style scoped>
.bg-primary {
  background-color: var(--prim-clr) !important;
}
</style>
