<!--
  Element+ for styling (https://element-plus.org/en-US/component/button.html)

  0. npm install element-plus --save
  1. Set the application to use Element+. Look at main.js (lines 3,4 and 10).
  2. npm install
  3. npm run serve
-->

<template>
  <div>
    <element-plus-example></element-plus-example>
  </div>
</template>

<script>
import ElementPlusExample from "./components/ElementPlusExample"

export default {
  // Write JavaScript here
  name: 'App',
  components: { ElementPlusExample },
}
</script>

<style>
  /* Write
    ElementPlusExample styling here */
</style>
