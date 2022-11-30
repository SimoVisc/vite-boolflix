<script>
    import axios from "axios";
    export default {
    name: "AppMain",
    components: {
    },
    created(){
        axios.get("https://api.themoviedb.org/3/movie/550?api_key=e28dd805ab0473696d4e9566a68c3d6e").then((res)=>{
            console.log(res.data)
        })
   }
}
</script>

<template>
    <main>
      
   </main>
</template>

<style lang="scss" scoped>
 
</style>