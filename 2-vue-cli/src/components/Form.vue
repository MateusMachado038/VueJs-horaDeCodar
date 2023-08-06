<template>
  <div>
    <form action="" @submit="enviarForm($event)">
      <div>
        <input type="text" v-model="name" />
      </div>
      <div>
        <input type="text" v-model="email" />
      </div>

      <div>
        <input-text-vue />
      </div>
      <submit-vue />
    </form>
    <p>Conteudos</p>
    <p>Conteudos</p>
    <p>Conteudos</p>
  </div>
</template>

<script>
import InputTextVue from "./Form/InputText.vue";
import SubmitVue from "./Form/Submit.vue";

export default {
  name: "Form-vue",
  components: {
    InputTextVue,
    SubmitVue,
  },
  data() {
    return {
      name: "",
      email: "",
    };
  },
  methods: {
    enviarForm(e) {
      e.preventDefault();

      const name = this.name;
      const email = this.email;

      console.log("Formulario enviado!");
      console.log("O nome é: " + name);
      console.log("O nome é: " + email);
    },
  },
};
</script>

<style scoped>
p {
  margin: 80px;
}
</style>
