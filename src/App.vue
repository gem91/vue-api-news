<template>
  <div id="app">
    <h1>API NEWS LISTS</h1>
    <div class="wrap">
      <toolBar></toolBar>
      <routerView></routerView>
    </div>
  </div>
</template>

<script>
import ToolBar from "./components/ToolBar.vue";
export default {
  components: {
    ToolBar,
  },
};
</script>

<style>
  body, * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  #app{
    margin: 100px auto;
    width: 50%;
  }
  h1{
    text-align: center;
  }
  .wrap{
    margin-top: 50px;
    border: 1px solid #f2efef;
    border-radius: 10px;
    overflow: hidden;
  }
</style>
