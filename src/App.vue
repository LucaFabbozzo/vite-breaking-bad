
<script>
import AppHeader from './components/AppHeader.vue'
import AppSearch from './components/AppSearch.vue'
import CharacterList from './components/CharacterList.vue';
import { axios } from 'axios';
  
export default {
  name: 'App',
  components: { AppHeader, AppSearch, CharacterList },
  data() {
    return {

    }
  },
  methods: {
    getCharacters() {
      // https://www.breakingbadapi.com/api/characters
      axios.get('https://www.breakingbadapi.com/api/characters')
        .then(result => {
          console.log(result.data);
        })
        .catch(error => {
          console.log(error);
        })
    }
  },
  mounted() {
    this.getCharacters();
  }
}

</script>

<template>
    <header>
      <AppHeader title="Breacking Bad Api"/> 
    </header>
    <div class="container m-auto my-4 w-75">
      <main>
        <AppSearch/>
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
