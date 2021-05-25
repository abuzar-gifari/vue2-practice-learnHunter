<template>
  <div class="profile">
    <h1>Profile User id {{ userId }}</h1>
  </div>
</template>

<script>
export default {
  name: 'profile',
  data () {
    return {
      userId : this.$route.params.user_id
    }
  },
  methods:{
    updateId(){
      this.userId = this.$route.params.user_id
    }
  },
  watch:{
    $route: 'updateId'
  }
}
</script>


<style>
h1{
  color:red;
}
</style>
