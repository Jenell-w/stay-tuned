<template>
  <div id="app">
    <h2>Watch out! It is coming for you!</h2>
    <img alt="coronavirus img" src="./assets/covid_19_graphic_generic.jpeg" />
    <StayInformed title="Stay Tuned for Quarantine Best Practices!!" />
    <a href="http://www.nytimes.com">NyTimes</a>
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
