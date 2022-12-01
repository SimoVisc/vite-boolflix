<script>
import { store } from "./store";
import axios from "axios";
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  },
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
    },
  // getData(){
  //   axios.get("https://api.themoviedb.org/3/search/tv", {
  //     params: {
  //       api_key: "e28dd805ab0473696d4e9566a68c3d6e",
  //       query: this.store.text,
  //       language: "it-IT"
  //   },
  //   })
  //   .then((res) => {
  //     console.log(res)
    //   this.store.series = res.data.results
    // })
    // .catch((err) =>{
  }
  }
</script>

<template>
    <AppHeader  @performSearch= "getData"/>
    <AppMain/>
    <AppFooter/>
</template>

<style lang="scss">
@import './style/global.scss';
</style>
