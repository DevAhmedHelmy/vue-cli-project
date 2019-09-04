<template>
  <div class="hello">
    <app-header :posts='posts'></app-header>
    <h1>{{ msg }}</h1>

  </div>
</template>

<script>
import Header from "./Header.vue";
export default {
  name: "HelloWorld",
  components:{
    'app-header':Header
  },
  data (){
    return{
      msg:'hello',
      posts:[
          {name:'jhdklsdjhsdk',title:'fjsjdfg;js'},
          {name:'jhdklsdjhsdk',title:'fjsjdfg;js'},
          {name:'jhdklsdjhsdk',title:'fjsjdfg;js'},
          {name:'jhdklsdjhsdk',title:'fjsjdfg;js'},
          {name:'jhdklsdjhsdk',title:'fjsjdfg;js'},
      ]
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
