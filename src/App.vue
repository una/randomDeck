<template>
  <div id="app">
    <heading v-bind:slideNum=slideNum></heading>
    <randomizer></randomizer>
  </div>
</template>

<script>
import Heading from './components/Header'
import Randomizer from './components/Randomizer'

export default {
  name: 'app',

  created: function () {
    document.addEventListener('keydown', this.slideCount)
  },

  methods: {
    slideCount: function (e) {
      if (e.keyCode === 32) {
        console.log(this.slideNum);
        this.slideNum++;
      }
    }
  },

  data () {
    return {
      slideNum: 1
    }
  },

  components: {
    Heading,
    Randomizer
  }
}
</script>

<style lang='scss'>
  $color--copy: #2c3e50;
  $color--accent: #c69;

  #app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: $color--copy;
    margin-top: 60px;
  }
</style>
