<template>
    <div>
      <h2>Recipes Found</h2>
      <div v-if="recipes.length">
        <RecipeCard v-for="recipe in recipes" :key="recipe.id" :recipe="recipe" />
      </div>
      <div v-else>
        <p>No recipes found with the given ingredients.</p>
      </div>
    </div>
  </template>
  
  <script>
  import RecipeCard from "./RecipeCard.vue";
  
  export default {
    props: ["recipes"],
    components: {
      RecipeCard,
    },
  };
  </script>
  
  <style scoped>
  h2 {
    margin-top: 20px;
  }
  </style>
  