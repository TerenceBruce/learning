<!-- 
========================
Watching Multiple Values
========================
  To watch multiple values, just place the values in an array.

=================
Watching an Array
=================
1. Use a function to return the array we want to watch (not passed in directly).
2. Return a copy of the values of the array.

===========================================
Watching Nested Properties of a Data Object 
===========================================

  When watching a specific property in a reactive object, the first argument you pass to watch() 
  will be an anonymous function that returns the specific property you want to watch.
-->

<template>
  <div>
    <h2>Full name is {{ first_name }} {{ last_name }}</h2>
    <br />

    <h1>Deep Watcher</h1>

    <div>
      <h4>{{ product.label }}</h4>
      <h5>£{{ product.price }} (£{{ discount }} Off)</h5>
    </div>

    <br />
    <el-button type="primary" @click="updatePrice">Reduce Price!</el-button>
  </div>
</template>

<script>
import { ref, reactive, watch } from "vue"

export default {
  setup() {
    // 1. Watching Multiple Values
    const first_name = ref("John");
    const last_name = ref("Smith");
    watch([first_name, last_name], (newValue, oldValue) => {
      console.log(newValue);
      console.log(oldValue);
    });

    first_name.value = "Jack";


    // 2. Watching an Array
    const level = ref([1, 2, 3, 4]);
    watch(() => [...level.value], (newValue, oldValue) => { // ...level.value returns a opy of the array
      console.log(newValue);
      console.log(oldValue);
    });

    level.value[3] = 111;


    // 3. Watching Nested Properties of a Data Object
    let discount = ref(0);
    let product = reactive({
      price: 25,
      label: 'Blue juice',
    });

    function updatePrice() {
      if (product.price < 1) 
        return
      product.price--;
    }

    watch(() => product.price, (newValue, oldValue) => {
      console.log(newValue)      
      console.log(oldValue)
      discount.value++;
    });

    return {level, discount, product, updatePrice, first_name, last_name }
  }
};
</script>

<style> 
</style>
