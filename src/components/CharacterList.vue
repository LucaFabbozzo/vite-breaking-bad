  <script>
  export default {
    name: 'CharacterList'
  }
  </script>

<template>
  <div class="container-cards">
    <div class="found">Found 62 characters</div>
  </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
  .container-cards {
    background-color: $secondary-color;
    width: 100%;
   .found {
    background-color: $primary-color;
    color: $secondary-color;
    height: 40px;
   }
  }
</style>