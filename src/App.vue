<template>
  <div id="app">
    <Menu v-if="!$route.meta.menu" />
    <router-view />
  </div>
</template>

<script>
  import Menu from '../src/components/Menu'
  export default {
    name: 'App',
    components:{
      Menu
    }
  }
</script>
<style>
  body{
   background-color: #f0ebeb;
   font-family: "Roboto","Lucida Grande","DejaVu Sans","Bitstream Vera Sans",Verdana,Arial,sans-serif;
  }
</style>
