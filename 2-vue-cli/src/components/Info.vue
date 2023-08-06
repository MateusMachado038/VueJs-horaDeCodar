<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <p>Utilizo as seguintes tecnologias para back-end</p>
    <!-- <ul v-for="(tecnology, index) in backend_tecnoloogies" v-bind:key="index">
      <li>{{ tecnology }}</li>
    </ul> -->
    <ul>
      <li v-for="(tecnology, index) in backend_tecnologies" v-bind:key="index">
        {{ tecnology }}
      </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para front-end</p>
    <ul>
      <li v-for="technology in frontend_tecnologies" :key="technology.id">
        {{ technology.language }}
      </li>
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
      backend_tecnologies: ["JavaScript", "PHP", "Python"],
      frontend_tecnologies: [
        { id: 1, language: "HTML" },
        { id: 2, language: "css" },
        { id: 3, language: "bootstrap" },
      ],
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
