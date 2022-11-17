  <script>
  export default {
  name: 'CharacterCard',
  props: {
      character: Object
    }
  }
  </script>

<template>
  <!-- img status -->
  <div class="sc-card col-3">
    <img :src="character.img" :alt="character.name">
    {{character.name}}
  </div>
</template>


<style lang="scss" scoped>

</style>