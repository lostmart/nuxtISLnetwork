<template>
  <div>
    <NavBar />
    <main>
      <Nuxt />
    </main>
    <FooterComp />
  </div>
</template>

<style>
main {
  min-height: 325px;
}
.page-enter-active,
.page-leave-active {
  transition: opacity 0.2s;
}
.page-enter,
.page-leave-to {
  opacity: 0;
}

.layout-enter-active,
.layout-leave-active {
  transition: opacity 0.2s;
}
.layout-enter,
.layout-leave-to {
  opacity: 0;
}
</style>
