  <script>
  export default {
  name: 'CharacterCard',
  data() {
    return {
      cardTitle: 'Bracking Bad'
    }
  },
  props: {
      character: Object
    }
  }
  </script>

<template>
  <!-- img status -->
  <div class="sc-card col-3">
    <img :src="character.img" :alt="character.name">
    <h3>{{character.name}}</h3>
    <p>{{cardTitle}}</p>
    <p>{{character.status}}</p>
  </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
.sc-card {
  text-align: center;
  background-color: #2E3946;
  width: 212px;
  padding-bottom: 21px;
  padding-top: 14px;
  margin: 20px auto;
  img {
    width: 170px;
  }
  h3 {
    color: $secondary-color;
    text-transform: uppercase;
    font-size: 0.9rem;
    padding-top: 15px;
    padding-bottom: 15px;
  }

  p {
    color: #535458;
    margin: 0;
    font-weight: lighter;
  }
}

</style>