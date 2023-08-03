<template>
  <div>
    <h2>Está é a descrição da pessoa: {{ nome }}</h2>
    <p>Estou trabalhando no momento.</p>
  </div>
  <InfoVue />
</template>

<script>
import InfoVue from "./Info.vue";

export default {
  name: "Pessoa-vue",
  components: {
    InfoVue,
  },
  data() {
    return {
      nome: "Mateus",
    };
  },
};
</script>
