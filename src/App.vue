<script>
import axios from "axios";
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  components: {
    AppHeader,
    AppMain,
    AppFooter,
  }
};
  axios.get("https://api.themoviedb.org/3/movie/", {
    params: {
      api_key: "e28dd805ab0473696d4e9566a68c3d6e",
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
