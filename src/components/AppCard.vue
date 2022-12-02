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
    }
   }
</script>

<template>
    <ul>
        <li>{{ info.title}}</li>
        <li>{{ info.original_title}}</li>
        <li><span :class="`fi fi-${getFlag(info.original_language)}`"></span></li>
        <li>{{ info.vote_average}}</li>
    </ul>
</template>

<style lang="scss">
</style>