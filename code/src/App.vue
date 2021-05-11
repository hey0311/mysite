<template>
  <div id="app">
    <Header></Header>
    <router-view/>
    <Footer></Footer>
    <GoTop></GoTop>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
body{
  font-family: Arial,sans-serif;
}
#app{
  padding-top: 160px;
}
</style>
