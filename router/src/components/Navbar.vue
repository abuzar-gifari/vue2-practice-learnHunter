<template>
  <div id="navbar">
    <nav>
      <ul>
        <li><router-link to="/">Home</router-link></li>
        <li><router-link to="/about">About</router-link></li>
        <li><router-link to="/contact">Contact</router-link></li>
      </ul>
    </nav>
    <button @click="contact">Contact</button>
    <button @click="about">About</button>
    <button @click="front">go</button>
    <button @click="back">back</button>
  </div>
</template>

<script>
export default {
  name:'navbar',
  data(){
    return{

    }
  },
  methods:{
    contact(){
      this.$router.push( {name:contact} )
    },
    about(){
      this.$router.push( {name:about} )
    },
    front(){
      this.$router.go(1)
    },
    back(){
      this.$router.go(-1)
    }
  }
}
</script>


<style>
nav{
  text-align: center;
}
nav ul{
  padding: 0;
}
nav li{
  display: inline-block;
  list-style-type: none;
  margin:0px;
  padding:8px;
}
</style>
