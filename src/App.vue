  
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
    <header>
      <AppHeader title="Breacking Bad Api"/> 
    </header>
    <div class="container">
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
