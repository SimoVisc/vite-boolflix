<script>
  import { store } from "../store";
    
  export default {
   name: "AppHeader",
  data() {
      return {
        store,
      }
    }
  }
</script>
 
<template>
    <h1>boolflix</h1>
    <form class="search-bar">
      <input 
      type="text"  
      placeholder="Search in Boolflix" 
      v-model= "store.text"
      required
      />
      <button @click="$emit('performSearch')">Search</button>
    </form>
</template>

<style lang="scss" scoped>
</style>