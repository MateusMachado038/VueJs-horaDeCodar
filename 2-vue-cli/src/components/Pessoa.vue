<template>
  <div>
    <h2>Está é a descrição da pessoa: {{ nome }}</h2>
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
