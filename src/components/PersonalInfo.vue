<template>
  <div class="personalInfo-wrap">
    <div class="cube">
      <ul>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'PersonalInfo',
  data () {
    return {
    }
  }
}
</script>

<style scoped lang="stylus">
.personalInfo-wrap {
  width 100%
  height 100vh
  background-color #696969
  overflow hidden
  .cube {
    ul {
      position relative
      top 200px
      width 200px
      height 200px
      transform-style preserve-3d
      margin 100px auto
      animation run 5s infinite linear
      li {
        list-style none
        width 200px
        height 200px
        position absolute
        left 0
        top 0
        opacity 1
      }
      li:first-child {
        background-color red
        background-size 100%
        transform translateZ(100px)
      }
      li:nth-child(2) {
        background-color blue
        background-size 100%
        transform translateY(-100px) rotateX(90deg)
      }
      li:nth-child(3) {
        background-color green
        background-size 100%
        transform translateY(100px) rotateX(90deg)
      }
      li:nth-child(4) {
        background-color white
        background-size 100%
        transform translateX(-100px) rotateY(90deg)
      }
      li:nth-child(5) {
        background-color orange
        background-size 100%
        transform translateX(100px) rotateY(90deg)
      }
      li:nth-child(6) {
        background-color yellow
        background-size 100%
        transform translateZ(-100px)
      }
    }
    @keyframes run {
      0% {
        transform rotateX(0deg) rotateY(0deg)
      }
      100% {
        transform rotateX(360deg) rotateY(360deg)
      }
    }
  }
}
</style>
