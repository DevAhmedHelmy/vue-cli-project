<template>
  <div id="addBlog">
      <h2>Add The New Blog</h2>
      <form>
        <label class="label">Blog Title:</label>

        <input type="text" v-model="blog.title" required>
        <label for="">Blog Content:</label>
        <textarea name="name" rows="8" cols="80" v-model="blog.content"></textarea>

      </form>



      <div id="preview">
        <h3>Preview Blog</h3>
        <p>Blog Title: {{blog.title}}</p>
        <p>Blog Content: {{blog.content}}</p>
      </div>
  </div>
</template>

<script>
  export default{
    data(){
      return{
        blog:{
          title:"",
          content:""
        }

      }
    }
  }
</script>
<style>
  #addBlog *{
    box-sizing:border-box;
  }
  #addBlog{
    margin: 20px auto;
    max-width: 500px;
  }
  label{
    display:block;
    margin: 20px 0 10px;
  }
  input[type="text"], textarea{
    display:block;
    width: 100%;
    padding: 8px;
  }
  #preview{
    padding: 10px 20px;
    border:1px dotted #ccc;
    margin: 3px 0
  }
  h3{
    margin: 10px;
  }

</style>
