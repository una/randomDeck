<template>
  <header>
    <h1>{{ title }}</h1>
    <p>{{ slideNum }}/10</p>
  </header>
</template>

<script>
export default {
  name: 'heading',
  props: ['slideNum'],

  data () {
    return {
      title: 'Topic Here'
    }
  }
}
</script>

<style scoped lang="scss">
  h1 {
    color: hotpink;
  }
</style>
