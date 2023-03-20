<template>
  <ul class="lists">
    <li v-for="user in users" :key="user">{{ user.title }}</li>
  </ul>
</template>

<script>
import { fetchNewsList } from "../api/index.js";

export default {
  data() {
    return {
      users: [],
    };
  },
  created() {
    fetchNewsList()
      .then((response) => (this.users = response.data))
      .catch((error) => console.log(error));
  },
};
</script>

<style scoped>
  @import "./contents.css";
</style>