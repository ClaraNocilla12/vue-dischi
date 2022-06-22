<template>
  <div id="app">

  

    <HomePage/>
 
  </div>
</template>

<script>
import HomePage from './components/HomePage.vue';

import 'bootstrap';

export default {
  name: 'App',
  components: {
    HomePage
    
  }
}
</script>

<style lang="scss">
@import "bootstrap/dist/css/bootstrap.min.css";
  body{
    margin: 0;
     background-color: rgb(58, 69, 87);
  }

</style>
