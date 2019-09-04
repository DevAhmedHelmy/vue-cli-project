<template>
   <header>
     <h1>Hello in Hedaer</h1>
     <ul>
       <li v-for="post in posts">
         {{post.name}}
       </li>
     </ul>
   </header>
</template>

<script>

export default {
    props:['posts']

};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

h1 {
  color: #42b983;
}
</style>
