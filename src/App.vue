<template>
  <div id="app">
    <header-main></header-main>
    <div class="main">
      <keep-alive>
        <transition enter-active-class="magictime twisterInUp" leave-active-class="magictime magic" mode="out-in">
          <router-view></router-view>
        </transition>
      </keep-alive>
    </div>
    <control-player></control-player>
    <detail-player></detail-player>
  </div>
</template>

<script>
import HeaderMain from './components/header/header-main'
import ControlPlayer from './components/control-player'
import DetailPlayer from './components/detail-player'
export default {
  components: {
    HeaderMain,
    ControlPlayer,
    DetailPlayer
  }
}
</script>

<style lang="less" scoped>
#app {
  .main {
    margin-top: 94px;
  }
}
</style>
