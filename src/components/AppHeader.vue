  <script>
  export default {
  name: 'AppHeader',
  props: {
    title: String
    }
  }
  </script>

<template>
    <img src="../assets/img/Breaking_Bad_logo.svg" alt="Logo">
    <h1>{{title}}</h1>
</template>


<style lang="scss" scoped>
  @use '../styles/partials/variables' as *;
  img {
    filter: invert(0%);
    width: 50px;
  }
  h1 {
    display: inline-block;
    color: $secondary-color;
    font-family: 'Syne Mono', monospace;
  }
</style>