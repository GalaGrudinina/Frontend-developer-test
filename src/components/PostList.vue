<template>
<form @submit.prevent>
<div class="absolute">
     <post-item
     v-for="post in posts"
    :post="post"
     :key="post.id"/>
     
</div>
 </form>
</template>

<script>
import PostItem from "@/components/PostItem";
export default {
    components:{PostItem},
props:{
    posts:{
        type: Array,
        required: true
    }

}} 
</script>

<style scoped>
.user-list-item {
  display: grid;
 
}
.user-list-enter-active,
.user-list-leave-active {
  transition: all 0.4s ease;
}
.user-list-enter-from,
.user-list-leave-to {
  opacity: 0;
  transform: translateX(130px);
}
.user-list-move {
  transition: transform 0.4s ease;
}

.absolute{
  position: absolute;
  top: 80px;
  right: 70%;
  width: 0px;
  display: flex;
  height: 100vh;
  flex-flow: column;
  flex-basis: 100%;
  flex-wrap: wrap;
}





</style>
