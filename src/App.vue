<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Header />
    <QuestionsBox />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import QuestionsBox from "./components/QuestionsBox";

export default {
  name: "app",
  components: {
    Header,
    QuestionsBox
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
