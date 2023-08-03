<template>
  <div>
    <form action="">
      <div>
        <input-text-vue />
      </div>
      <div>
        <input-text-vue />
      </div>
      <submit-vue />
    </form>
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
};
</script>
