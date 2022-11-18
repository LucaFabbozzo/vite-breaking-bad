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
      this.$emit('startFilter');
      }
    }
  }
  </script>

<template>
  <div class="container">
    <div class="row py-5">
      <div class="col-auto">
        <select v-model="store.categoryToSearch" class="form-select" aria-label="Default select example">
        <option value="" selected>Select Series</option>
        <option value="Breaking Bad">Breaking Bad</option>
        <option value="Better Call Saul">Better Call Saul</option>
      </select>
      </div>
      <div class="col-auto">
        <button @click="$emit('startFilter')" class="btn btn-dark">Search</button>
      </div>
      <div class="col-auto">
        <button @click="reset()" class="btn btn-light">Reset</button>
      </div>
    </div>
  </div>
</template>


<style lang="scss" scoped>

</style>