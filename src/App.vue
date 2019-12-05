<template>
  <div id="app">
    <ListContainer />
  </div>
</template>

<script>
import ListContainer from "./components/ListContainer.vue";

export default {
  name: "app",
  components: {
    ListContainer
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
