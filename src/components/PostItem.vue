<template>
     <div class="post">
    <div id="postPicture">{{post.picture}}</div>
    <div id="postTitle"><strong>{{post.title}} </strong></div>
    <div>{{post.body}}</div>
    <div><strong>{{post.price}}</strong></div>
    </div>
</template>

<script>
export default {
    props:{
      post:{
       type:Object,
       required:true,   
      }  
    }
}
</script>
 <style scoped>
 .post{
width: 330px;
height:400px;
margin: 4px;
position: relative;
background-color: #d2dae3;
padding: 10px;
border-style: solid;
top: 45px; 
    }


 </style>