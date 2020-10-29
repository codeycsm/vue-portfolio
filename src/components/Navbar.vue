<template>
  <div id="navContainer">
    <nav id="navbar">
      <a href="#" id="nav-brand" @click="changePage('about-me')"
        >Codey McDaniel</a
      >
      <ul>
        <li v-if="page !== 'about-me'">
          <a href="#" @click="changePage('about-me')">About</a>
        </li>
        <li v-if="page !== 'portfolio'">
          <a href="#" @click="changePage('portfolio')">Portfolio</a>
        </li>
        <li>
          <a href="../documents/Resume.pdf" target="_blank">Resume</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  props: ["page"],
  name: "Navbar",
  methods: {
    changePage(page) {
      this.$emit("changePage", page);
    },
  },
};
</script>

<style scoped>
#nav-container {
  width: 100%;
}
nav {
  background-color: #336b87;
}
a {
  text-decoration: none;
  color: #000;
}
li {
  display: inline;
  padding: 1em;
}
#navbar {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-around;
}
#nav-brand {
  font-size: 1.3em;
  padding: 1em;
}
</style>
