<template>
  <div class="header-wrap">
    <div class="navBar">
      <div class="logo">
        <img height="30px"
             width="126"
             :src="logoSrc" />
      </div>
      <div class="design"
           v-on:mouseover="setOverlay">
        <button @click="toDesign">毕设管理</button>
      </div>
      <div class="work"
           v-on:mouseenter="setOverlay">
        <button @click="toWork">就业对接</button>
      </div>
      <div class="bbs"
           v-on:mouseenter="setOverlay">
        <button @click="toBBS">论坛圈子</button>
      </div>
      <div class="user">

      </div>
    </div>
    <div class="overlay"
         v-if="showOverlay"
         v-on:mouseout="removeOverlay">
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      logoSrc: '#',
      showOverlay: false
    }
  },
  mounted () {
    this.getLogoSrc()
  },
  methods: {
    getLogoSrc () {
      this.logoSrc = require('../../assets/logo.png')
    },
    toDesign () {
      console.log('click')
    },
    toWork () {
      console.log('click')
    },
    toBBS () {
      console.log('click')
    },
    setOverlay () {
      this.showOverlay = true
    },
    removeOverlay () {
      this.showOverlay = false
    }
  }
}
</script>

<style lang="stylus" scoped>
.header-wrap {
  position relative
  overflow hidden
  height 100%
  .navBar {
    position absolute
    top 0
    width 100%
    height 50px
    background-color #9932CC
    display flex
    flex-flow row nowrap
    align-items center
    box-shadow 5px 1px 5px #A9A9A9
    z-index 200
    .logo {
      margin 0px 10px 0px 10px
    }
    .design {
      position relative
      color white
      text-align center
      margin 0 20px 0 20px
      font-weight bold
      flex 0 1 auto
      button {
        border none
        outline none
        background-color transparent
      }
    }
    .design::before {
      content ''
      position absolute
      bottom 0px
      left 0px
      border solid 2px white
      border-width 0 0 2px 2px
      width 10px
      height 10px
      transition 0.4s
      opacity 0
    }
    .design::after {
      content ''
      position absolute
      top 0px
      right 0px
      border solid 2px white
      border-width 2px 2px 0 0
      width 10px
      height 10px
      transition 0.4s
      opacity 0
    }
    .design:hover::before {
      bottom -5px
      left -7px
      opacity 1
    }
    .design:hover::after {
      top -5px
      right -7px
      opacity 1
    }
    .design:hover {
      background-color white
      color #9932CC
    }
    .work {
      position relative
      color white
      text-align center
      margin 0 20px 0 20px
      font-weight bold
      flex 0 1 auto
      button {
        border none
        outline none
        background-color transparent
      }
    }
    .work::before {
      content ''
      position absolute
      bottom 0px
      left 0px
      border solid 2px white
      border-width 0 0 2px 2px
      width 10px
      height 10px
      transition 0.4s
      opacity 0
    }
    .work::after {
      content ''
      position absolute
      top 0px
      right 0px
      border solid 2px white
      border-width 2px 2px 0 0
      width 10px
      height 10px
      transition 0.4s
      opacity 0
    }
    .work:hover::before {
      bottom -5px
      left -7px
      opacity 1
    }
    .work:hover::after {
      top -5px
      right -7px
      opacity 1
    }
    .work:hover {
      background-color white
      color #9932CC
    }
    .bbs {
      position relative
      color white
      text-align center
      margin 0 20px 0 20px
      font-weight bold
      flex 0 1 auto
      button {
        border none
        outline none
        background-color transparent
      }
    }
    .bbs::before {
      content ''
      position absolute
      bottom 0px
      left 0px
      border solid 2px white
      border-width 0 0 2px 2px
      width 10px
      height 10px
      transition 0.4s
      opacity 0
    }
    .bbs::after {
      content ''
      position absolute
      top 0px
      right 0px
      border solid 2px white
      border-width 2px 2px 0 0
      width 10px
      height 10px
      transition 0.4s
      opacity 0
    }
    .bbs:hover::before {
      bottom -5px
      left -7px
      opacity 1
    }
    .bbs:hover::after {
      top -5px
      right -7px
      opacity 1
    }
    .bbs:hover {
      background-color white
      color #9932CC
    }
  }
  .overlay {
    width 100%
    height 200px
    background-color white
    position absolute
    top 50px
    animation overlayCreate 0.5s linear
    opacity 1
    box-shadow 5px 1px 5px #A9A9A9
    z-index 100
  }
  .overlay::before {
    content ''
    position absolute
    top -250px
    opacity 0
    z-index 100
  }
  @keyframes overlayCreate {
    0% {
      top -250px
      opacity 0
    }
    100% {
      top 50px
      opacity 1
    }
  }
}
</style>
