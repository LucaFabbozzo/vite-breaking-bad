  <script>
import { store } from '../data/store';

export default {
  name: 'CharacterList',
  data() {
    return {
      store
    }
  }
}
  </script>

<template>
  <div class="container-cards">
    <ul>
      <li v-for="character in store.charactersListData" :key="character.char_id">
        {{character.name}}
      </li>
    </ul>
  </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
  .container-cards {
    background-color: $secondary-color;
    width: 100%;
  }
  li {
    color: black;
  }
</style>