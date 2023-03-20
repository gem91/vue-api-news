<template>
  <ul class="lists">
    <li v-for="item in ask" :key="item">{{ item.title }}</li>
  </ul>
</template>

<script>
import { fetchAskList } from "../api/index.js";

export default {
  data() {
    return {
      ask: [],
    };
  },
  created() {
    fetchAskList()
      .then((response) => (this.ask = response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style scoped>
  @import "./contents.css";
</style>