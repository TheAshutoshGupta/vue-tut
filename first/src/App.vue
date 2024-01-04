<template>
    <div id="container">
      <Navbar/>
      <router-view></router-view>
    </div>
</template> 

<script setup>
  import Navbar from './components/HomePage/Navbar.vue';
 import Home from './views/Home.vue'
</script> 

<style>
#container{
  padding-left: 3%;
  padding-right: 3%;
}
</style> 