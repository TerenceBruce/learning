<template>
  <div>
    <h1>Looping Through Arrays</h1>
    <ul>
      <li v-for="n in 5" :key="n">
        {{ n }}
      </li>
    </ul>
    <ul>
      <li v-for="(item, n) in interests_array" :key="n">
        {{ item }}
      </li>
    </ul>
  </div>
</template>

<script>
export default {
    setup() {
      const interests_array = ["Scientific computing", "Artificial Intelligence", "Functional Programming"];

      return { interests_array }
    }
};
</script>

<style>
</style>
