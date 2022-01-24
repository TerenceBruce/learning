<!--
=====================================
TASK: INTERPOLATION WITH CONDITIONALS
=====================================
0. npm install
1. npm run serve
2. In the MyComponent.vue component, which is in the 'components' folder:
    a. Add the 'setup' function entry point to the 'script' block/section. 
    In the setup function:
      b. Add a data variable called 'title' with the string value "Interpolation in My First Component!!!". 
      c. Save the file. The data title should appear on the web page.
    
    d. In Vue, interpolation will resolve any JavaScript inside curly braces. 
       For example, you can transform your text inside the curly braces using 
       the toUpperCase() method:

       {{ title.toUpperCase() }}

       Do this and confirm that the title is all in uppercase. Remember, this is all in MyComponent.vue!
    
    e. In addition to parsing JavaScript methods, interpolation can handle conditional logic. 
       Create a boolean data variable in the 'setup' function called 'isUppercase' and initiliasie it to 'false'.
    f. As we want access the 'isUppercase' variable in the HTML template section, remember to 'return'/expose it 
       in the 'setup' function. 
       If you don't, the HTML template section will not know about it.
    g. In the HTML template block/section, replace the previous interpolation with the following conditional logic:

       {{ isUppercase ? title.toUpperCase() : title }}

       This is shorthand for:
          if (isUpperCase == true)
            title.toUpperCase()
          else
            title

    h. Save and confirm that the title is no longer all in uppercase.
    i. Play around by changing the 'isUpperCase' boolean variable to 'true'.
    j. Save and confirm that the title is now in uppercase.
-->

<template>
  <div>
    <my-component></my-component>
  </div>
</template>

<script>
import MyComponent from "./components/MyComponent";

export default {
  name: 'App',
  components: { MyComponent, },

  setup() {} 
}
</script>

<style>
  /* Write styling here */
</style>
