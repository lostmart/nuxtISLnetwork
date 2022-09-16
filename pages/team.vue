<template>
  <div class="container">
    <div class="card">
      <div class="card-body">
        <ul class="nav nav-tabs">
          <li class="nav-item">
            <button
              class="nav-link"
              :class="{ active: language === 'spanish' }"
              aria-current="page"
              @click="language = 'spanish'"
            >
              ES
            </button>
          </li>
          <li class="nav-item">
            <button
              class="nav-link"
              :class="{ active: language === 'english' }"
              aria-current="page"
              @click="language = 'english'"
            >
              EN
            </button>
          </li>
        </ul>
        <TeamCompSp v-if="language === 'spanish'" />
        <TeamCompEng v-if="language === 'english'" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "ISL network equipo",
      language: "spanish",
    };
  },
  head() {
    return {
      title: this.title,
      link: [
        {
          rel: "stylesheet",
          href: "https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.13.0/css/all.min.css",
        },
      ],
    };
  },
};
</script>

<style>
.padrinos-voluntarios p {
  margin-bottom: 0.2em;
}
.img-laura {
  max-width: 325px;
}
</style>
