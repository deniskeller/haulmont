<script>
export default {  
  components: {
  },
};
</script>

<template>
  <div class="header">
    <img class="header__logo" src="@/assets/img/spacex.svg" alt="" srcset="">
    <div class="header__title">Space <span>X</span><br>Missions</div>    
  </div>
</template>

<style lang="scss" scoped>
.header {
  padding-top: em(209px);
  padding-bottom: em(84px);
  @include ifmobile {
    padding-top: em(70px);
    padding-bottom: em(40px);
  }
  &__logo {
    width: em(324px);
    height: em(40px);
    margin-bottom: em(40px);
    @include ifmobile {
      width: em(242px);
      height: em(30px);
    }
  }
  &__title {
    font-size: em(180px);
    line-height: 90%;
    font-weight: 300;
    letter-spacing: 1.7px;
    color: $blue;
    span{
      color: $white;
    }
    @include ifmobile {
font-size: em(120px);
    }
  }
}
  
</style>
