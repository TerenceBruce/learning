<template>
  <div>
    <h1>Shop Watcher</h1>

    <div>
      Black Friday sale
      <strike>Was {{ old_discount }}%</strike>
      <strong> Now {{ discount }}% OFF</strong>
    </div>

    <br />
    <el-button type="primary" @click="updateDiscount">Increase Discount!</el-button>
  </div>
</template>

<script>
import { ref, watch } from "vue"

export default {
  setup() {
    const old_discount = ref(0)
    const discount = ref(5);

    function updateDiscount() {
      discount.value = discount.value + 5;
    }

    watch(discount, (newValue, oldValue) => {
      old_discount.value = oldValue;
    });

    return { old_discount, discount, updateDiscount }
  }
};
</script>

<style> 
</style>
