<!--
  VUE DIRECTIVES: v-model
  Vue's `v-model` is a two-way data binding attribute.

  Consider what it means to bind a piece of data in two ways. 
  The context for this form of data model is usually forms, 
  or where you expect both input and output data. 
  
  
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
