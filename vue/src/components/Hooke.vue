<template>
<div id ="Hooke"> 
<h2>{{title}}</h2>
<button @click = "ChangeTitle">Click me</button>
</div>

</template>

<script>
export default {
    name:"Hooke",
   
    data(){
        return {
           title:'Hook Methos Data'
        }
    },
      mounted(){
            alert('mounted hook called')
    },
    beforeMount(){
          alert('beforeMount hook called')
    },
      created(){
           alert('created Hook ')
    },

    beforeCreate(){
    alert('beforeCreate hook')
    },
    updated(){
        alert('updated method call in  hook')
    },
    beforeUpdate(){
            alert('beforeUpdate hook')
    },
  
    methods:{
       ChangeTitle(){
           this.title  ='Youtube learing'
       }
    }
  
}
</script>
