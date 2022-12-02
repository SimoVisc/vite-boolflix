<script>
    export default {
    name: "AppCard",
    props:{
      info: Object
    },
    methods: {
        getFlag(lang) {
          if (lang === "en") {
               return "gb";
            } else if (lang === "ko") {
            return "kr";
          } else return lang;
        },
        vote(info) {
        return Math.ceil(info.vote_average / 2);
        }
    }
    }
</script>

<template>
    <ul>
        <li><img :src="`https://image.tmdb.org/t/p/w342${info.poster_path}`" alt=""></li>
        <li>{{ info.title}}</li>
        <li>{{ info.original_title}}</li>
        <li><span :class="`fi fi-${getFlag(info.original_language)}`"></span></li>
        <li>
            <i class="fa-solid fa-star" v-for="n in vote(info)"></i>
            <i class="fa-regular fa-star" v-for="n in (5 - vote(info))"></i>        
        </li>
    </ul>
</template>

<style lang="scss">
</style>