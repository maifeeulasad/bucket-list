<template>
  <div id="app">
    <!--
    <img alt="Bucket List Icon" src="./assets/logo.png">
    -->
    <HelloWorld
            title="My bucket-list"
            footer="MUA"
            link="https://maifeeulasad.github.io"

    />
  </div>
</template>

<script>
import HelloWorld from './components/BucketList.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
</style>
