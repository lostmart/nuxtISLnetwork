<template>
  <section class="container">
    <h2 class="text-center mt-4">Materiales</h2>
    <div class="row justify-content-around p-4">
      <div
        v-for="book in books"
        class="col-sm-2 alert alert-primary d-flex justify-content-center"
        role="alert"
      >
        <a target="_blank" :href="book.link">{{ book.title }}</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "materials",
  data() {
    return {
      title: "ISL network | materiales",
      books: [
        {
          title: "Libro Uno",
          link: "https://www.dropbox.com/s/gbklb3ue6m6tj1q/ISL%20LIBRO%201.pdf?dl=0",
        },
        {
          title: "Libro Dos",
          link: "https://www.dropbox.com/s/w5jz532z4c5m600/ISL%20BOOK%202.pdf?dl=0",
        },
        {
          title: "Flashcards",
          link: "https://www.dropbox.com/s/muz5zyfwxq9dme5/Flashcards%20ISL%20A%C3%91O%201%202022.pdf?dl=0",
        },
        {
          title: "Flashcards II",
          link: "https://www.dropbox.com/s/pip7qlpfksthqy5/ISL%20Flashcards%20A%C3%91O%202.pdf?dl=0",
        },
      ],
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
a {
  text-decoration: none;
}
</style>
