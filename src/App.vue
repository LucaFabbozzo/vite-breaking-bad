  
  <script>
import AppHeader from './components/AppHeader.vue'
import AppSearch from './components/AppSearch.vue'
import CharacterList from './components/CharacterList.vue';
  
  export default {
  name: 'App',
  components: { AppHeader, AppSearch, CharacterList }
  }
  </script>

<template>
  <div class="container">
    <AppHeader />
    <main>
      <AppSearch/>
      <CharacterList/>
    </main>
  </div>
</template>

<style lang="scss">
  @use './styles/general' as *;
</style>
