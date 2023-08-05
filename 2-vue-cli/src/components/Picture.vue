<template>
  <img :src="avatar" :alt="descricao" />
</template>

<script>
export default {
  name: "Picture_01",
  data() {
    return {
      avatar: "/img/avatar.png",
      descricao: "Mateus Alves Machado",
    };
  },
};
</script>
