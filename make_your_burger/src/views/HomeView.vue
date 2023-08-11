<template>
  <BannerVue />
  <div class="main-container">
    <h1>Monte o seu burger:</h1>
    <BurgerFormVue />
  </div>
</template>

<script>
import BannerVue from "@/components/Banner.vue";
import BurgerFormVue from "@/components/BurgerForm.vue";

export default {
  name: "Homevue",
  components: {
    BannerVue,
    BurgerFormVue,
  },
};
</script>
