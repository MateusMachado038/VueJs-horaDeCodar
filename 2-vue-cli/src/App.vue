<template>
  <life-cycle />
  <pessoa />
  <form-vue />
</template>

<script>
import FormVue from "./components/Form.vue";
import LifeCycle from "./components/LifeCycle.vue";
import Pessoa from "./components/Pessoa.vue";

export default {
  name: "App",
  components: { LifeCycle, Pessoa, FormVue },
};
</script>
