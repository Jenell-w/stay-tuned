<template>
  <div id="app">
    <img alt="coronavirus img" src="./assets/covid_19_graphic_generic.jpeg" />
    <StayInformed title="Stay Tuned for Quarantine Best Practices" />
  </div>
</template>

<script>
import StayInformed from "./components/StayInformed.vue";

export default {
  name: "App",
  props: ["title"],
  components: {
    StayInformed
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
