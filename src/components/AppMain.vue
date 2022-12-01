<script>
    import { store } from "../store";
    import AppCard from "./AppCard.vue";
    export default {
    name: "AppMain",
    components: {
      AppCard
    },
    data() {
      return {
        store,
      }
    },
}
</script>

<template>
  <AppCard v-for="movie in store.movies" :info="movie"/>
  
     <!-- <section class="movies-container">
         <ul>
             <li v-for="movie in store.movies" >{{movie.title}}</li>
          </ul>
     </section> -->
     <!-- <section class="series-container">
          <ul>
             <li v-for="serie in store.series" >{{serie.title}}</li>
          </ul>
        </section> -->
</template>

<style lang="scss" scoped>
 
</style>