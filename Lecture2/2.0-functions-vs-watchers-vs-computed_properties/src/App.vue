<!--
  Vue watchers programmatically observe component data and run whenever a particular property changes.
  
  Watched data can contain two arguments: oldVal and newVal. 
  This can help you when writing expressions to compare data before writing or binding new values. 
  
  Watchers can observe objects as well as string, number, and array types. 
  When observing objects, it will only trigger the handler if the whole object changes.

  Watchers complement the usage of computed data since they can passively observe values and cannot 
  be used like normal Vue data variables, while computed data must always return a value and can be 
  looked up.

  In this exercise, we will use watcher arguments to watch data for changes, then use this watcher 
  to set variables via a function/method.
-->

<template>
  <div>
    <watcher></watcher>
  </div>
</template>

<script>
import Watcher from "./components/Watcher.vue";

export default {
  // Write JavaScript here
  name: "App",
  components: { Watcher },
};
</script>

<style>
/* Write styling here */
</style>
