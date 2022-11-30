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
};
  axios.get("https://api.themoviedb.org/3/movie/550", {
    params: {
      api_key: "e28dd805ab0473696d4e9566a68c3d6e",
      query: this.store.text
   },
 })
  .then((res) => {
    console.log(res)
  });

  

</script>

<template>
    <AppHeader/>
    <AppMain/>
    <AppFooter/>
</template>

<style lang="scss">
@import './style/global.scss';
</style>
