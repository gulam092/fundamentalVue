<template>
<div>
	<nav>
     <ul>
       <li><a href="">Home</a></li>
       <li><a href="">Post</a></li>
       <li><a href="">About</a></li>
       <li><a href="">Contact</a></li>
    </ul>
    </nav>
</div>

</template>

<script>
export default {
    name:"Navbar"
  
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