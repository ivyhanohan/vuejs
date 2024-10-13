<template>
    <div>
      <input
        type="text"
        placeholder="Enter ingredients (comma-separated)"
        v-model="ingredientInput"
      />
      <button @click="findRecipes">Find Recipes</button>
      <RecipeList :recipes="filteredRecipes" />
    </div>
  </template>
  
  <script>
  import { recipes } from "../recipes";
  import RecipeList from "./RecipeList.vue";
  
  export default {
    components: {
      RecipeList,
    },
    data() {
      return {
        ingredientInput: "",
        filteredRecipes: recipes,
      };
    },
    methods: {
      findRecipes() {
        const ingredients = this.ingredientInput
          .toLowerCase()
          .split(",")
          .map((ingredient) => ingredient.trim());
        this.filteredRecipes = recipes.filter((recipe) =>
          ingredients.every((ingredient) =>
            recipe.ingredients.includes(ingredient)
          )
        );
      },
    },
  };
  </script>
  
  <style scoped>
  input {
    padding: 8px;
    margin-right: 10px;
  }
  button {
    padding: 8px;
  }
  </style>
  