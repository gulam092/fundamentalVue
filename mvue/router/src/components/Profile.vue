<template>
  <div class="Profile">
    <h2>This is Profile Page({{ UserID }})</h2>
  </div>
</template>

<script>
export default {
  name: 'Profile',
  data () {
    return {
     UserID:this.$route.params.user_id
    }
  },
  methods:{
      updateId(){
          this.UserID = this.$route.params.user_id
      }
  },
  watch:{
      $route: 'updateId'
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
h2{
    color: aqua;

}
</style>