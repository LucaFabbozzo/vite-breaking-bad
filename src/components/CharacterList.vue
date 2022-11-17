  <script>
import { store } from '../data/store';
import CharacterCard from './CharacterCard.vue'

export default {
  name: 'CharacterList',
  components: { CharacterCard },
  data() {
    return {
      store
    }
  }
}
  </script>

<template>
  <div class="container container-cards">
    <div class="row">
      <CharacterCard 
      v-for="character in store.charactersListData" 
      :key="character.char_id"
      :character="character"
      />
    </div>
  </div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
  .container-cards {
    background-color: $secondary-color;
    width: 100%;
    padding-right: 45px;
    padding-left: 45px;
  }

</style>