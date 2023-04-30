<template>
  <div>
    <h2 class="card-title mt-4">Nuestro equipo</h2>
    <div class="card mt-4">
      <div class="card-body">
        <h5 class="card-title text-center">COORDINACIÓN</h5>
        <div class="text-center">
          <img
            class="img-laura img-thumbnail"
            src="@/assets/laura-motta.jpg"
            alt="Laura Motta coordinadora"
          />
          <p class="card-text">Prof. Laura Motta</p>
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
          <div
            v-for="parent in godParents"
            :key="parent"
            class="col col-sm-6 col-lg-4"
          >
            <a :href="parent.linkedIn" target="_blank">
              <div class="alert alert-secondary" role="alert">
                <p>
                  <span>
                    <strong>{{ parent.name }}</strong>
                  </span>
                  <i v-if="parent.linkedIn" class="fab fa-linkedin"></i>
                </p>
                <p>{{ parent.descrip }}</p>
              </div>
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="card mt-4 mx-auto">
      <div class="card-body">
        <h5 class="card-title">Equipo de enlace ISL</h5>
        <div class="row">
          <div class="col-sm-12 col-md-6">
            <div class="row">
              <div v-for="card in team" :key="card" class="col">
                <div class="alert alert-secondary team-card" role="alert">
                  <p class="mb-1">
                    <strong>{{ card.name }}</strong>
                    <a :href="card.linkedIn" target="_blank">
                      <i class="fab fa-linkedin"></i>
                    </a>
                  </p>
                </div>
              </div>
            </div>
          </div>
          <div class="col-sm-12 col-md-6">
            <img src="@/assets/isl-20.jpg" alt="godparents around the world" />
          </div>
        </div>
      </div>
    </div>
    <hr />
    <a
      href="https://www.linkedin.com/in/martin-pedraza-7bb3bb89/"
      target="_blank"
    >
      <div
        class="alert alert-secondary mx-auto"
        role="alert"
        style="margin-bottom: 0"
      >
        <p>
          <span>
            <strong>Martin Pedraza</strong>
          </span>
          <i class="fab fa-linkedin"></i>
        </p>
        <p>Desarrollo web</p>
      </div>
    </a>
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
      godParents: [
        {
          name: "Julio Barreiro",
          descrip: "Departamentos de Flores y Lavalleja",
          linkedIn: "",
        },
        {
          name: "Cecilia Cabrera",
          descrip: "Departamento de Florida y Durazno",
          linkedIn: "https://www.linkedin.com/in/ceciliacabreramartirena/",
        },
        {
          name: "Maria Elena Schnyder",
          descrip: "Departamento de Colonia y San José",
          linkedIn:
            "https://www.linkedin.com/in/mar%C3%ADa-elena-schnyder-33b98362/",
        },
        {
          name: "Virginia Frade",
          descrip: "Departamento de Maldonado",
          linkedIn: "",
        },
        {
          name: "Laura Motta",
          descrip:
            "Departamentos de Soriano, Salto, Artigas, Rivera, Tacuarembó, Cerro Largo, Treinta y Tres",
          linkedIn: "",
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

a,
.fa-linkedin {
  text-decoration: none;
  color: #007cc3;
  font-size: 1.2rem;
  margin-left: 0.5em;
}

.alert-secondary {
  min-width: 130px;
  max-width: 334px;
  font-size: 0.85rem;
  min-height: 84px;
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  justify-content: space-around;
  align-items: center;
}
.alert-secondary p {
  margin-bottom: 0;
  display: flex;
  align-items: center;
  justify-content: space-around;
}
.team-card {
  display: flex;
  align-items: center;
  justify-content: space-evenly;
}
.team-card p {
  display: flex;
  align-items: center;
  justify-content: space-around;
  min-width: 215px;
  font-size: 1.1rem;
}
</style>
