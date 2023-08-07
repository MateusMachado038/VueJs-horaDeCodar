<template>
  <img :src="avatar" :alt="descricao" />
  <MudarImagem @mudar-imagem="mudarImagem" />
</template>

<script>
import MudarImagem from "./MudarImagem.vue";

export default {
  name: "Picture_01",
  components: {
    MudarImagem,
  },
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "Mateus Alves Machado",
    };
  },
  methods: {
    mudarImagem() {
      this.avatar = "/img/avatar2.png";
    },
  },
};
</script>
