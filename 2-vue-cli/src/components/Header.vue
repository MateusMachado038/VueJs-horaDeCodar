<template>
  <ul>
    <li>
      <a href="#">Home</a>
      <a href="#">Projetos</a>
      <a href="#">Contato</a>
    </li>
  </ul>
</template>

<script>
export default {
  // eslint-disable-next-line vue/multi-word-component-names
  name: "Header",
};
</script>

<style scoped>
ul {
  list-style: none;
  display: flex;
  background: #999;
}
li {
  margin-right: 16px;
}

a {
  color: #ddd;
  text-decoration: none;
  transition: 0.5s;
  padding: 20px;
}

a:hover {
  color: turquoise;
}
</style>
