<template>
  <div id="app">
    <h1><strong>Stop</strong> in the name of Light!</h1>

    <light v-on:lightClicked="catchLight"/>
  </div>
</template>

<script>
  import light from './components/light.vue';

  export default {
    name: 'app',
    components : {
      light
    },
    methods : {
      catchLight : catchLight
    },
    data () {
      return {
        msg: 'Welcome to Your Vue.js App'
      }
    }
  }

  function catchLight( color ) {    
    alert( 'light was clicked...' + color );    
  }
</script>

<style lang="scss">
  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
    margin-top: 60px;
  }

  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
