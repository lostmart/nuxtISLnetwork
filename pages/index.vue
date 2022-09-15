<template>
  <div class="container">
    <div class="card">
      <div class="card-body">
        <h1 class="card-title">Godparents Network Uruguay</h1>
        <div class="row">
          <div class="col-lg-6">
            <p class="card-text">
              Godparents es un proyecto de
              <strong>innovación social</strong> de servicios educativos,
              llevado a cabo por <strong>voluntarios</strong>, no hay cargos
              pagos en nuestra organización. Su funcionamiento es enteramente
              <strong>virtual.</strong> Brinda apoyo a las escuelas de las
              comunidades rurales de Uruguay y alcanza a más de
              <strong>4.500</strong> niños y niñas.
            </p>
            <p class="card-text eng">
              Godparents is a <strong>social innovation</strong> project for
              educational services, run entirely by
              <strong>volunteers.</strong>There are no paid positions in our
              organization. Its operation is entirely
              <strong>virtual.</strong> It provides support to schools in rural
              communities in Uruguay.<br />
              Godparents Project reaches over
              <strong>4,500</strong> children and adolescents
            </p>
          </div>
          <div class="col-lg-6 col-md-12 d-flex align-items-center">
            <img
              src="@/assets/Godparents_2022.jpg"
              alt="godparents around the world"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "IndexPage",
};
</script>

<style scoped>
img {
  width: 100%;
}
.card {
  position: relative;
  min-height: 400px;
  border: transparent !important;
}
.card .card-title {
  font-size: 2.2rem;
  text-shadow: 1px 2px grey;
  z-index: 1;
  text-align: center;
}

.card .card-text {
  font-size: 1.2rem;
}
.card .eng {
  top: 22rem !important;
}
@media (min-width: 768px) {
  .card .card-title {
    font-size: 2.9rem;
  }
}
</style>
