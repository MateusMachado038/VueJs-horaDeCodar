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
  </div>
</template>

<script>
export default {
  name: "Info-ok",
  data() {
    return { esta_trabalhando: false };
  },
};
</script>
