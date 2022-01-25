<template>
  <div class="container">
    <h1>Async fetch</h1>

    <el-button type="success" @click="getApi()">
      {{ loading ? "Loading..." : "Learn something profound" }}
    </el-button>
    <blockquote v-if="quote">{{ quote }}</blockquote>
  </div>
</template>

<script>
import { ref, computed } from "vue";
import axios from 'axios';

export default {
  setup() {
    let loading = ref(false);
    let axios_response = ref(null);

    let quote = computed( () => {
      return axios_response.value && axios_response.value.slip
        ? axios_response.value.slip.advice
        : null
    }); 

    function getApi() {
      loading.value = true
      return axios.get('https://api.adviceslip.com/advice').then(response => {
        axios_response.value = response.data
        console.log(axios_response.value)
        setTimeout(() => {
          loading.value = false
        }, 4000);
      })
    }
  
    return { loading, quote, getApi }
  }
};
</script>

<style>
  .el-button {
    margin: 5px;
  } 
</style>
