<template>
  <div id="app">
   <post-form
    @create="createPost"
   />
   <post-list 
   :posts="posts"
  />
  </div>
</template> 

<script>
import PostForm from "@/components/PostForm";
import PostList from "@/components/PostList";

export default {
  name: 'App',
  components: { 
    PostForm, PostList
    
  },
  data(){
    return{
      posts:[
        {id:1, picture:'Image',title:"Наименование товара", body:"Довольно-таки интересное описание товара в несколько строк. Довольно-таки интересное описание товара в несколько строк", price:"10 000 руб."},
      ],
    
    }
  },
  methods:{
    createPost (post){
this.posts.push(post);
    },
 
  }
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
 
}


</style>
