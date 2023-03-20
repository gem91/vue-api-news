<template>
  <ul class="lists">
    <li v-for="job in jobs" :key="job">{{ job.title }}</li>
  </ul>
</template>

<script>
import { fetchJobsList } from "../api/index.js";

export default {
  data() {
    return {
      jobs: [],
    };
  },
  created() {
    fetchJobsList()
      .then((response) => (this.jobs = response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style scoped>
  @import "./contents.css";
</style>