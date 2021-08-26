<template>

<div id="app">
  <top/>
  <div id="left">
  <leftside/>
  </div>
  <div id="right">
  <rightside/>
  </div>

</div>
</template>

<script>
import top from './components/top.vue'
import leftside from './components/leftside.vue'
import rightside from './components/rightside.vue'



export default {
  name: 'app',
  components: {
    top,
    leftside,
    rightside,
  }
}
</script>

<style>

#app {
  margin-left:-10px;
  margin-right: -10px;
  margin-top:-10px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

}

#left{
  margin-top:20px ;
  margin-left:10px ;
  width:800px;
  height: 100em;
 
}

#right{

  margin-top: -1610px;
  margin-left: 1704px;
 
}

</style>
