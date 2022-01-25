<!--
  Handling Search Functionality Using a Vue Method, a Watcher, and Computed Props
  ===
  In this exercise, we will create a component that allows users to search data arrays using three 
  different methods in Vue.

  By the end of the exercise, 
  after fixing all the errors, you should be able to see first-hand how each different method works.
-->

<template>
  <div>
    <functions-computed-watcher></functions-computed-watcher>
  </div>
</template>

<script>
import FunctionsComputedWatcher from "./components/FunctionsComputedWatcher.vue";

export default {
  // Write JavaScript here
  name: "App",
  components: { FunctionsComputedWatcher },
};
</script>

<style>
/* Write styling here */
</style>
