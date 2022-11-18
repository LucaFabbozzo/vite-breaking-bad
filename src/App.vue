
<script>
import AppHeader from './components/AppHeader.vue'
import AppSearch from './components/AppSearch.vue'
import CharacterList from './components/CharacterList.vue';
import axios from 'axios';
import {store} from './data/store'
  
export default {
  name: 'App',
  components: { AppHeader, AppSearch, CharacterList },
  data() {
    return {
      store
    }
  },
  methods: {
    getCharacters() {
      store.isLoaded = false;
      axios.get(store.apiUrl, {
        params: {
          category: store.categoryToSearch
        }
       })
         .then(result => {
           store.charactersListData = result.data;
           store.isLoaded = true;
        })
        .catch(error => {
          store.charactersListData = [];
          store.isLoaded = true;
          console.log(error);
        })
    }
  },
  mounted() {
      this.getCharacters() 
  }
}

</script>

<template>
    <header>
      <AppHeader title="Breacking Bad Api"/> 
    </header>
    <div class="container m-auto my-4 w-75">
      <main>
        <AppSearch @startFilter="getCharacters()"/>
        <CharacterList/>
      </main>
    </div>
</template>

<style lang="scss">
  @use './styles/general';
  header {
  display: flex;
  align-items: center;
  justify-content: flex-start;
  width: 95%;
  margin: 0 auto;
  }
</style>
