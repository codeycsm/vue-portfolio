<template>
  <div id="app">
    <navbar :page="page" v-on:changePage="changePage" />
    <component :is="page"></component>
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
import AboutMe from "./components/AboutMe";
import Portfolio from "./components/Portfolio";

export default {
  name: "App",
  components: {
    Navbar,
    AboutMe,
    Portfolio,
  },
  data() {
    return {
      page: "about-me",
    };
  },
  methods: {
    changePage(page) {
      this.page = page;
    },
  },
};
</script>

<style scoped></style>
