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
        <about-content-es v-if="language === 'spanish'"></about-content-es>
        <about-content-eng v-if="language === 'english'"></about-content-eng>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: "ISL network about",
      language: "spanish",
    };
  },
  head() {
    return {
      title: this.title,
    };
  },
};
</script>

<style scoped>
.padrinos-voluntarios p {
  margin-bottom: 0.2em;
}
.img-laura {
  max-width: 210px;
}
</style>
