<template>
  <section class="container">
    <h2 class="text-center mt-4">Materiales</h2>
    <div v-if="show" class="row justify-content-around p-4">
      <div
        v-for="book in books"
        class="col-sm-2 alert alert-primary d-flex justify-content-center"
        role="alert"
      >
        <a target="_blank" :href="book.link">{{ book.title }}</a>
      </div>
      <div class="mt-4">
        <a
          href="https://www.youtube.com/playlist?list=PLtupDLnojS6s_LeuiI141CCc8fctt1fgZ"
          target="_blank"
          >Youtube playlist</a
        >
      </div>
    </div>
    <div v-else>
      <h3 class="text-center mt-4">Contendio exclusivo para godparentes</h3>
      <form
        ref="formPass"
        class="w-50 mx-auto bg-primary p-4"
        @submit.prevent="handleSubmit"
      >
        <div class="mb-3">
          <label for="exampleInputPassword1" class="form-label mb-3"
            >Password</label
          >
          <input
            type="password"
            class="form-control"
            id="exampleInputPassword1"
            v-model="input"
          />
        </div>
        <button type="submit" class="btn btn-secondary">Submit</button>
      </form>
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
      cogin: "123456",
      show: false,
      input: "",
    };
  },
  head() {
    return {
      title: this.title,
    };
  },
  methods: {
    handleSubmit() {
      this.input === this.cogin ? (this.show = true) : this.handleError();
    },
    handleError() {
      this.$refs.formPass.classList.add("shake");
      setTimeout(() => {
        this.$refs.formPass.classList.remove("shake");
        this.input = "";
      }, 450);
    },
  },
};
</script>

<style scoped>
form {
  color: white;
}
.bg-primary {
  background-color: #418bd0 !important;
  border-radius: 0.375rem;
}

.btn-secondary {
  background-color: #f09f06 !important;
}

a {
  text-decoration: none;
}

.shake {
  animation: shake 0.2s infinite;
}

@keyframes shake {
  0% {
    transform: translateX(0);
  }
  25% {
    transform: translateX(-15px);
  }
  50% {
    transform: translateX(0);
  }
  75% {
    transform: translateX(10px);
  }
  100% {
    transform: translateX(0);
  }
}
</style>
