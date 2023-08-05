<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <p>Utilizo as seguintes tecnologias</p>
    <ul>
      <li>C#</li>
      <li>Python</li>
      <li>Javascript</li>
      <li>PHP</li>
    </ul>
    <div>
      <button @click="showEmail">{{ textBtn }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para {{ email }}</p>
    <p>
      Para acessar meu portifóli
      <a v-bind:href="meu_link" target="_blank">basta clicar aqui!</a>
    </p>
    <PictureVue />
  </div>
</template>

<script>
import PictureVue from "./Picture.vue";

export default {
  name: "Info-ok",
  components: {
    PictureVue,
  },
  data() {
    return {
      mostrar_email: true,
      esta_trabalhando: false,
      email: "teste@gmail.com",
      meu_link: "https://google.com",
      textBtn: "Mostrar e-mail",
    };
  },
  methods: {
    showEmail() {
      this.mostrar_email = !this.mostrar_email;
      if (!this.mostrar_email) {
        this.textBtn = "Mostrar e-mail";
      } else {
        this.textBtn = "Esconder e-mail";
      }
    },
  },
};
</script>
