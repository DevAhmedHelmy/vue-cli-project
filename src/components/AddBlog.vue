<template>
  <div id="addBlog">
      <h2>Add The New Blog</h2>
      <form>
        <label class="label">Blog Title:</label>

        <input type="text" v-model.lazy="blog.title" required>
        <label for="">Blog Content:</label>
        <textarea name="name" rows="8" cols="80" v-model.lazy="blog.content"></textarea>
        <div id="checkboxs">
          <label class="label">check 1 :</label>
          <input type="checkbox" name="" value="check 1"
            v-model="blog.categories">
          <label class="label">check 2:</label>
          <input type="checkbox" name="" value="check 2"
            v-model="blog.categories">
          <label class="label">check 3:</label>
          <input type="checkbox" name="" value="check 3"
            v-model="blog.categories">
          <label class="label">check 4:</label>
          <input type="checkbox" name="" value="check 4"
            v-model="blog.categories">
          <label class="label">check 5:</label>
          <input type="checkbox" name="" value="check 5"
            v-model="blog.categories">
        </div>
        <label>Slect One</label>
        <select v-model="blog.author" name="">
            <option v-for="author in blog.authors">{{author}}</option>

        </select>
      </form>



      <div id="preview">
        <h3>Preview Blog</h3>
        <p>Blog Title: {{blog.title}}</p>
        <p>Blog Content: {{blog.content}}</p>

        <ul>
          <li v-for="category in blog.categories">{{category}}</li>
        </ul>
      </div>
  </div>
</template>

<script>
  export default{
    data(){
      return{
        blog:{
          title:"",
          content:"",
          categories:[],
          author:"",
          authors:['ahmed','sayed','hahah','dhdhgdg']
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
  #checkboxs input{
    display:inline-block;
    margin-right: 10px;
  }
  #checkboxs label{
    display: inline-block;
  }

</style>
