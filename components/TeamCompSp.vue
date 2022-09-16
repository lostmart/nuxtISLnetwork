<template>
  <div>
    <h2 class="card-title mt-4">Nuestro equipo</h2>
    <div class="card mt-4">
      <div class="card-body">
        <h5 class="card-title">COORDINACIÓN</h5>
        <div class="row">
          <div class="col-4 d-flex align-items-center">
            <p class="card-text">Prof. Laura Motta</p>
          </div>
          <div class="col-6 d-flex align-items-center">
            <img
              class="img-laura img-thumbnail"
              src="@/assets/laura-motta.jpg"
              alt="Laura Motta coordinadora"
            />
          </div>
        </div>
      </div>
    </div>
    <div class="card mt-4">
      <div class="card-body">
        <p class="card-text">
          Los referentes son docentes de inglés como lengua extranjera de
          diversas procedencias y formaciones que conocen el contexto en el que
          se desarrolla el Proyecto Godparents.
        </p>
        <p class="card-text">
          Trabajan voluntariamente con grupos de padrinos cuyas escuelas se
          encuentran en un mismo territorio o departamento.
        </p>
        <h4 class="mb-n2">Ellos son:</h4>
        <div class="row padrinos-voluntarios">
          <!--  loop to fill this  -->
        </div>
      </div>
    </div>
    <div class="card mt-4 mx-auto">
      <div class="card-body">
        <h5 class="card-title">Equipo de enlace ISL</h5>
        <div class="row">
          <div class="col-12 col-md-6">
            <div class="row">
              <div v-for="card in team" :key="card" class="col col-sm-12">
                <div class="alert alert-secondary" role="alert">
                  <p class="mb-1">
                    <strong>{{ card.name }}</strong>
                    <a :href="card.linkedIn" target="_blank">
                      <i class="fab fa-linkedin"></i>
                    </a>
                  </p>
                </div>
              </div>
              <!---
              <div class="col col-sm-12">
                <div class="alert alert-secondary" role="alert">
                  <p class="mb-1">
                    <strong>Prof. Florencia Perez</strong>
                    <a
                      href="https://www.linkedin.com/in/mar%C3%ADa-florencia-p%C3%A9rez-784134216/"
                      target="_blank"
                    >
                      <i class="fab fa-linkedin"></i>
                    </a>
                  </p>
                </div>
              </div>
              <div class="col col-sm-12">
                <div class="alert alert-secondary" role="alert">
                  <p class="mb-1">
                    <strong>Mta. Valentina Alpuin</strong>
                    <a
                      href=" https://www.linkedin.com/in/valentinaalpuin/"
                      target="_blank"
                    >
                      <i class="fab fa-linkedin"></i>
                    </a>
                  </p>
                </div>
              </div>
              <div class="col col-sm-12">
                <div class="alert alert-secondary" role="alert">
                  <p class="mb-1">
                    <span>
                      <strong>Prof. Valentina Dubini</strong>
                    </span>
                    <a
                      href="https://www.linkedin.com/in/valentinadubini/"
                      target="_blank"
                    >
                      <i class="fab fa-linkedin"></i>
                    </a>
                  </p>
                </div>
              </div>
              -->
            </div>
          </div>
          <div class="col-12 col-md-6">
            <img src="@/assets/isl-20.jpg" alt="godparents around the world" />
          </div>
        </div>
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
      team: [
        {
          name: "Dr. Aldo Rodriguez",
          linkedIn: "https://www.linkedin.com/in/aldo-rodriguez-45515937",
        },
        {
          name: "Prof. Florencia Perez",
          linkedIn:
            "https://www.linkedin.com/in/mar%C3%ADa-florencia-p%C3%A9rez-784134216/",
        },
        {
          name: "Mta. Valentina Alpuin",
          linkedIn: "https://www.linkedin.com/in/valentinaalpuin/",
        },
        {
          name: "Prof. Valentina Dubini",
          linkedIn: "https://www.linkedin.com/in/valentinadubini/",
        },
      ],
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

<style scoped>
img {
  width: 100%;
}

.alert-secondary {
  min-width: 130px;
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
.alert-secondary p {
  display: flex;
  align-items: center;
  justify-content: space-around;
  gap: 2rem;
  min-width: 215px;
}
</style>
