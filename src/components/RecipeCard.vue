<template>
    <div class="recipe-card">
      <h3>{{ recipe.title }}</h3>
      <p><strong>Ingredients:</strong> {{ recipe.ingredients.join(", ") }}</p>
      <p><strong>Instructions:</strong> {{ recipe.instructions }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: ["recipe"],
  };
  </script>
  
  <style scoped>
  .recipe-card {
    border: 1px solid #ddd;
    padding: 15px;
    margin: 10px 0;
  }
  </style>
  