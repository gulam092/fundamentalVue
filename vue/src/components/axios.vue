<template>
<div id ="axios"> 
<h2> Post Axios</h2><hr>
<input type="" v-model="searchTerm" placeholder="search">
<div v-for="data in filtersearch" :key ="data.id">
    <h3>{{data.title}}</h3>
    <p>{{data.body | snippet}}</p>
</div>

</div>

</template>

<script>
import axios  from 'axios';
export default {
    name:"axios",
   
    data(){
        return {
         post:[],
         searchTerm:''
        }
    },
    computed:{
      filtersearch(){
          return this.post.filter(data =>{
              return data.title.match(this.searchTerm)
          })
      }
    },
   
  
    methods:{
     
    },
    created(){
        axios.get('https://jsonplaceholder.typicode.com/posts').then(response => {
            this.post = response.data
        })
        .catch(error =>{
            console.log(error)
        })
    }
  
}
</script>
<style>
h2{
    color: blueviolet;
    text-align: center;
}
</style>