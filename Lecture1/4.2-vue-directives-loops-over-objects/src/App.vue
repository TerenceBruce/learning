<!--
  When requesting data from an API, you will often be iterating over an array of objects 
  that contains both logic and raw content. 
  
  Vue makes it easy to control the data's various states through its directive syntax. 
  
  Conditional directives control the display state of DOM elements in Vue. 
  
  The HTML syntax provides clear visibility when it comes to the display rules set in your component.
-->

<template>
  <div>
    <vue-directives></vue-directives>
  </div>
</template>

<script>
import VueDirectives from "./components/VueDirectives.vue";

export default {
  // Write JavaScript here
  name: "App",
  components: { VueDirectives },
};
</script>

<style>
/* Write styling here */
</style>
