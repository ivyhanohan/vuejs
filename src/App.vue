<template>
  <div id="app">
    <h1>Recipe Finder</h1>
    <RecipeFinder />
  </div>
</template>

<script>
import RecipeFinder from "./components/RecipeFinder.vue";

export default {
  name: "App",
  components: {
    RecipeFinder,
  },
};
</script>

<style>
#app {
  text-align: center;
  padding: 20px;
}
</style>
