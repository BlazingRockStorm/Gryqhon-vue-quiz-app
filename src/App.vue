<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Header />
    <b-container class="bv-example-row">
      <b-row>
        <b-col sm="6" offset="3">
          <QuestionsBox />
        </b-col>
      </b-row>
    </b-container>
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
  },
  mounted: function() {
    fetch("https://opentdb.com/api.php?amount=10&category=12&type=multiple", {
      method: "get"
    }).then(response => {
      console.log(response.json());
    });
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
