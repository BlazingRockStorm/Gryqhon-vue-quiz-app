<template>
  <div class="question-box-container">
    <b-jumbotron>
      <template v-slot:lead v-html="innerHTML">
        {{ decodeHtml(currentQuestion.question) }}
      </template>

      <hr class="my-4" />

      <p>
        List of answers
      </p>

      <b-button variant="primary" href="#">Submit</b-button>
      <b-button @click="next" variant="success">Next</b-button>
    </b-jumbotron>
  </div>
</template>

<script>
export default {
  name: "QuestionsBox",
  props: {
    currentQuestion: Object,
    next: Function
  },
  mounted() {
    console.log(this.currentQuestion)
  },
  data() {
    return {};
  },
  methods: {
    decodeHtml: function (html) {
      var txt = document.createElement("textarea");
      txt.innerHTML = html;
      return txt.value;
    }
  },
  computed: {}
};
</script>

<style>
</style>
