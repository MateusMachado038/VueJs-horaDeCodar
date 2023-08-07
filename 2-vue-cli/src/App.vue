<template>
  <div>
    <Header :esta_logado="true" />
    <PrimeiroComponenteVue />
    <life-cycle />
    <pessoa />
    <form-vue />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import FormVue from "./components/Form.vue";
import LifeCycle from "./components/LifeCycle.vue";
import Pessoa from "./components/Pessoa.vue";
import PrimeiroComponenteVue from "./components/PrimeiroComponente.vue";

export default {
  name: "App",
  components: { LifeCycle, PrimeiroComponenteVue, Pessoa, FormVue, Header },
};
</script>

<style>
body {
  background-color: #333;
  color: #fff;
}

a {
  color: red;
}
</style>
