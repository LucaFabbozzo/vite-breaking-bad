  <script>
  import {store} from '../data/store'
  export default {
  data() {
      return {
        store
      }
  },
  methods: {
    reset() {
      store.categoryToSearch = '';
      }
    }
  }
  </script>

<template>
  <div class="container">
    <div class="row">
      <div class="col-auto">
        <select v-model="store.categoryToSearch" class="form-select" aria-label="Default select example">
        <option value="" selected>Select Series</option>
        <option value="Breaking Bad">Breaking Bad</option>
        <option value="Better Call Saul">Better Call Saul</option>
      </select>
      </div>
      <div class="col-auto">
        <button @click="$emit('startFilter')" class="btn btn-info">Search</button>
      </div>
      <div class="col-auto">
        <button @click="reset()" class="btn btn-warning">Reset</button>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>

</style>