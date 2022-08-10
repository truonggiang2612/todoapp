<template>
    <div class="app">
      <component-content/>
      <component-slide-menu/>
    </div>
</template>

<script>
import ComponentContent from './components/ComponentContent.vue'
import ComponentSlideMenu from './components/ComponentSlideMenu.vue'


export default {
  name: 'App',
  components: {
    ComponentContent,
    ComponentSlideMenu
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

body {
    font-family: Arial, Helvetica, sans-serif;
    color: #fff;
    background-color: #2c3e50;
}

* {
  box-sizing: border-box;
}
</style>
