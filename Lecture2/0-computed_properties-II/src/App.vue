<!--
  Instances where you may use a computed property include but are not limited to:
    Combining data props:
    In the following example, you can use computed props to combine two pieces of data into one 
    returnable string, formalName, that can be used within your component:
-->

<template>
  <div>
    {{ formalName }}
  </div>
</template>

<script>
import { ref, computed } from "vue";

export default {
  // Write JavaScript here
  name: "App",

  setup() {
    const title = ref("Mr");
    const surname = ref("Smith");

    const formalName = computed( () => {
      return title.value + " " + surname.value;
    })

    return { formalName }
  },
};
</script>

<style>
/* Write styling here */
</style>
