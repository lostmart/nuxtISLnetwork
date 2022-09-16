<template>
  <div class="container">
    <h2 class="text-center">FAQ</h2>
    <AccordeonComp
      title="What is Inglés Sin Límites? / ¿Qué es Inglés Sin Límites?"
      id="headingOne"
      collapsNo="collapseOne"
    />
    <AccordeonComp
      title="What is the Godparents Project? / ¿Qué es el Proyecto de
								Padrinos y Madrinas?"
      id="headingTwo"
      collapsNo="collapseTwo"
    />
    <AccordeonComp
      title="How is ISL implemented? / ¿Cómo se implementa ISL?"
      id="headingThree"
      collapsNo="collapseThree"
    />
    <AccordeonComp
      title="How is ISL fully implemented in the classroom? ¿Cómo se implementa ISL en el aula al 100%?"
      id="headingFour"
      collapsNo="collapseFour"
    />
  </div>
</template>

<script>
export default {
  data() {
    return {
      title: "ISL network FAQ",
    };
  },
  head() {
    return {
      title: this.title,
    };
  },
};
</script>
