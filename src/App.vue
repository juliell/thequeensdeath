<template style="margin: 0px;">
  <div id="app">
    <Header />
    <Disclaimer />
    <Timeline />
  </div>
</template>

<script>
import Disclaimer from './components/Disclaimer.vue'
import Header from './components/Header.vue'
import Timeline from './components/Timeline.vue'
import 'vue-js-modal/dist/styles.css'

export default {
  name: 'App',
  components: {
    Timeline,
    Header,
    Disclaimer,
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: -4em;
}
</style>
