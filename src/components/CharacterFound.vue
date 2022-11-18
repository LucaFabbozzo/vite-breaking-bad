  <script>
  import {store} from '../data/store'
export default {
  name: 'CharacterFound',
  data() {
    return {
      store
    }
  },
  computed: {
    outputResult() {
      if (store.charactersListData.length > 0) {
        return store.charactersListData.length;
      }
      return 'No result'
    }
  }
}
  </script>

<template>
  <div class="found">Found {{outputResult}} characters</div>
</template>


<style lang="scss" scoped>
@use '../styles/partials/variables' as *;
  .found {
    background-color: #202528;
    color: #ffffff;
    padding: 10px 15px;
    width: 100%;
  }
</style>