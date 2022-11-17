  <script>
  export default {
  name: 'CharacterCard',
  props: {
      character: Object
    }
  }
  </script>

<template>
  <div class="sc-card">
    {{character.name}}
  </div>
</template>


<style>

</style>