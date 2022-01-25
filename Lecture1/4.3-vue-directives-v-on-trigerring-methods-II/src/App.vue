<!--
  Often in a web application, we want elements to appear on the page depending on whether 
  a condition is met or not. 
  
  For instance, if our product is not in stock, our page should display the fact that 
  it is out of stock.

  We will conditionally render elements depending on whether our product is in stock or not.
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
