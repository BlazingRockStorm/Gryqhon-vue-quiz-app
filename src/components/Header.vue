<template>
  <div>
    <b-nav tabs>
      <b-nav-item disabled>
        <b>Gryqhon's Quiz App</b>
      </b-nav-item>
      <b-nav-item disabled>Counter: {{numCorrect}}/{{numTotal}}</b-nav-item>
    </b-nav>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["numCorrect", "numTotal"],
  mounted() {},
  data() {
    return {};
  },
  methods: {},
  computed: {}
};
</script>

<style>
</style>
