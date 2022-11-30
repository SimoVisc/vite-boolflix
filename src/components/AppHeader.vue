<script>
  
    
  export default {
   name: "AppHeader",
   
  }
</script>
 
<template>
  <header >
    <h1>boolflix</h1>
    <form class="search-bar">
      <div>
        <input 
        type="text"  
        placeholder="Search in Boolflix"
        v-model="store.text"
        />
        <button type="submit" >Search</button>
      </div>
    </form>
 </header>
</template>

<style lang="scss" scoped>
</style>