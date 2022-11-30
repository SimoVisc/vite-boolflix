<script>
    import { store } from "../store";
    export default {
    name: "AppMain",
    components: {
    },
    data() {
      return {
        store,
      }
    },
}
</script>

<template>
    <main>
     <section class="movies-container">
         <ul>
             <li v-for="movie in store.movies" >{{movie.title}}</li>
          </ul>
     </section>
     <section class="series-container">
         <ul>
             <li v-for="serie in store.series" >{{serie.title}}</li>
          </ul>
     </section>
   </main>
</template>

<style lang="scss" scoped>
 
</style>