<template>
  <div id="app">
    <div class="container">
      <img class="cosmonaut" src="@/assets/img/cosmonaut.png">
      <Header/>
      <Missions/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header';
import Missions from './components/Missions';

export default {
  name: "App",
  components: {
    Header,
    Missions,
  },
};
</script>

<style lang="scss">
@import "./assets/scss/main";
#app {
  padding-left: 15px;
  padding-right: 15px;
  padding-bottom: em(158px);
  @include ifmobile {
    padding-left: 30px;
    padding-right: 30px;
    padding-bottom: em(40px);
    overflow: hidden;
  }
  .container {
    position: relative;
    .cosmonaut {
      position: absolute;
      z-index: -1;
      top: 0;
      right: 0;
      width: em(734px);
      height: em(916px);
      @include ifmobile {
        width: em(734px);
        right: 50%;
        transform: translate(50%, 0);
      }
    }
  }
}
</style>
