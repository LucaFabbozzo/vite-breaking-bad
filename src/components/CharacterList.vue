  <script>
import { store } from '../data/store';
import CharacterCard from './CharacterCard.vue'
import CharacterFound from './CharacterFound.vue'
import AppLoading from './AppLoading.vue'

export default {
  name: 'CharacterList',
  components: { CharacterCard, CharacterFound, AppLoading },
  data() {
    return {
      store
    }
  }
}
  </script>

<template>
  <div class="container py-5 container-cards">
    <CharacterFound />
    <div v-if="store.isLoaded" class="row">
      <CharacterCard 
      v-for="character in store.charactersListData" 
      v-show="character.img != '' "
      :key="character.char_id"
      :character="character"
      />
    </div>
    <div v-else>
      <AppLoading />
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