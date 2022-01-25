<template>
  <div>
    <!-- In the two input elements below, create a two-way binding to the first_name and last_name. -->
    <input ? placeholder="First name" />
    <input ? placeholder="Last name" />

    <h3>{{ fullName }}</h3>
  </div>
</template>

<script>
import { ?, ? } from "vue" // Fix

export default {
    setup() {
      const first_name = ""; // Fix
      const last_name = "";  // fix

      // Create a 'computed' function fullName that returns a
      // concatenation of the first_name and the last_name. 
      const fullName = ???(  
        ???
      );

      return { ?, ? } // Fix
    }
};
</script>

<style> 
</style>
