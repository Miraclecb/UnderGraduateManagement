<template>
  <div class="home-wrap">
    <Header></Header>
  </div>
</template>

<script>
import Header from './universal/Header'

export default {
  name: 'Home',
  components: {
    Header
  }
}
</script>

<style scoped lang="stylus">
.home-wrap {
  width 100%
  height 100vh
}
</style>
