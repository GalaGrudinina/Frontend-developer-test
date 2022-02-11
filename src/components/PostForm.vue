<template>
    <div class="relative">
  <h1><strong> Добавление товара</strong></h1>
<form @submit.prevent>
          <div>
          <label for="picture">Ссылка на изображение товара</label>
          <input required
          id="picture"
          v-model="post.picture" 
          class="input"
   type="text" 
   placeholder="Введите ссылку">
  </div>

<div>
<label for="title">Наименование товара</label>
   <input required
   id="title"
   v-model="post.title" 
   class="input"
   type="text" 
   placeholder="Наименование товара">
  </div>  

    <div> 
<label for="body">Описание товара</label>
  <textarea
  id="body"
  v-model="post.body" 
  class="input"
   type="text" 
   placeholder="Введите описание товара"
   ></textarea>
        </div> 
  <div>
  <label for="price">Цена товара</label><br>
  <input required  
  id="price"
   v-model="post.price" 
   class="input"
   min="1"
   type="number" 
    placeholder="Введите цену">
  </div>    
  <button 
  class="btn" 
  @click="createPost">Добавить товар</button>
        </form>
      </div>
</template>

<script>
 export default {
data(){
    return{
       post:{
picture: "",
title:'',
body:'',
price:''
       } 
    }
},
methods:{
    createPost(){
      
  this.post.id= Date.now();
this.$emit('create', this.post,)
this.post={
picture : '',
title :'',
body :'',
price :''
}

    }
}

 }  
</script>

<style scoped>
#body{
  height:130px;
}
form {
  position: relative;
  width: 332px;
  height: 440px;
 width: 250px;
 border-style: solid;
}
input:invalid:required {
border: 2px solid rgb(228, 12, 12);
}
input:valid {
border: 2px solid black;}
.btn{
   margin: 20px;
}
h1{
    text-align: left;
}

</style>