<template>
  <div>
    <button @click="primeiro(txt1, $event), segundo($event)">
      Ativar Multiplos Eventos
    </button>
    <p>{{ multiplos_eventos }}</p>
  </div>
</template>

<script>
export default {
  name: "MultiplosEventos",
  data() {
    return {
      multiplos_eventos: "",
      txt1: "Primeiro Evento",
    };
  },
  methods: {
    primeiro(txt1, e) {
      e.preventDefault();

      this.multiplos_eventos = txt1;
    },
    segundo(e) {
      e.preventDefault();
      setTimeout(() => (this.multiplos_eventos = "Segundo evento!"), 500);
    },
  },
};
</script>

<style scoped>
div {
  margin: 100px;
}
</style>
