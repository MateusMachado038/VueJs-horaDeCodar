<template>
  <div>
    <NavBarVue :logo="logo_src" :alt="app_name" />
    <router-view />
    <FooterVue />
  </div>
</template>

<script>
import NavBarVue from "./components/NavBar.vue";
import FooterVue from "./components/Footer.vue";

export default {
  components: {
    NavBarVue,
    FooterVue,
  },
  data() {
    return {
      logo_src: ".//assets/img/logo.png",
      app_name: "Mae Your Burger",
    };
  },
};
</script>

<style>
* {
  font-family: Arial, Helvetica, sans-serif;
  padding: 0;
  margin: 0;
  box-sizing: border-box;
}

.main-container {
  margin: 50px;
  min-height: 250px;
}

h1 {
  text-align: center;
  font-size: 42px;
  margin-bottom: 30px;
  color: #222;
}
</style>
