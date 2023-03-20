<template>
  <header class="header">
    <router-link to="/news">News</router-link>
    <router-link to="/ask">Ask</router-link>
    <router-link to="/jobs">Jobs</router-link>
  </header>
</template>

<style scoped>
.header {display: flex;padding: 20px 20px;background: #42b883;}
.header a{position: relative; margin-right: 25px;font-size: 1rem;color: #fff; font-weight: bold; transition: all 3s ease-in-out;}
.header a:before{content: ''; position: absolute; top: 5px; left: -13px; width: 1px; height: 60%; background: #fff;}
.header a:first-child:before{ display: none; }
</style>