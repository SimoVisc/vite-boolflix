<script>
  import { store } from "../store";
  import axios from "axios";
    
  export default {
    name: "AppHeader",
    data() {
      return {
        store,
      }
    },
    methods:{
      getData(){
        axios.get("https://api.themoviedb.org/3/search/movie", {
          params: {
            api_key: "e28dd805ab0473696d4e9566a68c3d6e",
            query: this.store.text,
            language: "it-IT"
          },
        })
        .then((res) => {
          this.store.movies = res.data.results
        })
        axios.get("https://api.themoviedb.org/3/search/tv", {
         params: {
           api_key: "e28dd805ab0473696d4e9566a68c3d6e",
           query: this.store.text,
           language: "it-IT"
          },
       })
       .then((res) => {
        this.store.series = res.data.results
      })
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
      <button type="button" @click="getData">Search</button>
    </form>
</template>

<style lang="scss" scoped>
</style>