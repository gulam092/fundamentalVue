<template>
<div>
	<nav>
     <ul>
       <li><router-link to="/">Home</router-link></li>
       <li><router-link to="/about">About</router-link></li>
       <li><router-link to="/contact">Contact</router-link></li>
    </ul>
    </nav>
    <div>
        <ul>
            <li v-for="(id ,index) in userIds" :key ="index">
            <router-link :to="{name:'Profile',params:{user_id: id}}">
                Profile {{ id }}
            </router-link>
            </li>
        </ul>
        <button @click ="ContactUs">Contact us</button>
        <button @click ="AboutUs">About  us</button>

    </div>
</div>

</template>

<script>
export default {
    name:"Navbar",
    data(){
        return {
            userIds :['1','2','3','4','5','6','7','8','9','10']
        }
    },
    methods:{
        ContactUs(){
                  this.$router.push({ name:'Contact' })
        },
        AboutUs(){
            this.$router.push({ name:'About' })
        }
    },

  
}
</script>
<style scoped>
	nav ul {
		padding:0;

	}
	nav li {
        color: blueviolet;
		display :inline-block;
		margin: 0;
        list-style: none;
        padding: 8px;
		
	}
</style>
