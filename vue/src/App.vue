<template>
  <div id="app">
   <h2>{{title}}</h2>
   <Navbar></Navbar>
   <axios></axios>
   <!-- <Hooke></Hooke> -->
      <!-- <AllFriends :friends ="friends" @delete ="deleteFriend"></AllFriends>
    <OnlineFriends :friends ="friends"></OnlineFriends> -->
 
    <div>
	
</div>
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue' 
import Navbar from './components/Navbar.vue';
import axios from  './components/axios.vue';
// import Hooke from './components/Hooke.vue'
// import OnlineFriends from './components/OnlineFriends.vue';
// import AllFriends from './components/AllFriends.vue';

export default {
  name: 'App',
  data(){
    return {
      title:"This is our Component!",
      //  friends:[
      //           {name:'A',online:true},
      //           {name:'B',online:false},
      //           {name:'C',online:true},
      //           {name:'D',online:false},
      //           {name:'E',online:false},
      //       ]
    }
  },
  components: {
    // HelloWorld
    Navbar,
    axios,
    // OnlineFriends,
    // AllFriends

  },
  methods:{
    // deleteFriend(payload){

    //      //console.log(payload);
    //      this.friends = this.friends.filter(friend =>{
    //        return friend.name !== payload.name
    //       })
    // }
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

