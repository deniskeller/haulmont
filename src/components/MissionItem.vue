<template>
  <div class="mission">
    <img class="mission__image" :src="require(`@/assets/img/${image}`)" alt="">
    <h3 class="mission__subtitle">{{ subtitle }}</h3>

    <span><h1 class="mission__title">{{ title }}</h1></span>

    <div>
      <p v-for="p in paragraph" :key="p.index" class="mission__text" :class="{ pb: paragraph.length > 1}">{{ p }}</p>
    </div>

    <div class="mission__appointed">
      <div class="mission__appointed__item mission__appointed--date">
        <img src="@/assets/img/calendar.svg" alt="">
        <p>{{ appointed_date }}</p>
      </div>
      <div class="mission__appointed__item mission__appointed--time">
        <img src="@/assets/img/clock.svg" alt="">
        <p>{{ appointed_time }}</p>
      </div>
      <div class="mission__appointed__item mission__appointed--rocket">
        <img src="@/assets/img/rocket.svg" alt="">
        <p>{{ appointed_rocket }}</p>
      </div>
    </div>    
  </div>
</template>

<script>
export default {
  name: "MissionItem",
  props: {
    subtitle: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      default: ''
    },
    image: {
      type: String,
      default: ''
    },
    paragraph: {
      type: Array,
      default: null
    },
    appointed_date: {
      type: String,
      default: ''
    },
    appointed_time: {
      type: String,
      default: ''
    },
    appointed_rocket: {
      type: String,
      default: ''
    },
  }
};
</script>
<style scoped lang="scss">
.mission{
  width: 100%;
  background: $grey;
  padding: em(60px) em(70px) em(60px) em(290px);
  position: relative;
  @include ifmobile {
    padding: em(20px) em(20px) em(40px) em(20px);
  }  
  &__image {
    position: absolute;
    top: em(50px);
    left: em(50px);
    width: em(180px);
    height: em(180px);
    @include ifmobile {
      display: none;
    }
  }
  &__subtitle {
    font-size: em(24px);
    letter-spacing: 7px;
    line-height: 100%;
    color: $blue;
    margin-bottom: em(16px);
  }
  span {
    display: block;
    max-width: em(630px);
    margin-bottom: em(40px);
    @include ifmobile {
      margin-bottom: em(20px);
    }
  }
  &__title {
    font-size: em(72px);
    line-height: 100%;
  }
  &__text {
    font-size: em(18px);
    line-height: 140%;
    font-family: $Ubuntu;
    max-width: em(690px);
  }
    &__text:last-child {
      margin-bottom: em(40px);
      @include ifmobile {
        margin-bottom: em(20px);
      }
    }

  &__appointed {
    display: flex;
    flex-direction: row;
    align-items: center;
    @include ifmobile {
      flex-wrap: wrap;
    }
    &__item {
      position: relative;
      padding-left: em(42px);      
      display: flex;
      align-items: center;
      margin-right: em(30px);
      height: em(32px);
      @include ifmobile {
        width: 100%;
        margin-right: 0;
        margin-bottom: em(10px);
      }
      p {
        font-size: em(24px);
        line-height: 100%;
        letter-spacing: 2px;
      }
      img {
        display: block;
        position: absolute;
        left: 0;
        top: 0;
        width: em(32px);
        height: em(32px);
        display: block;
      }
    }
    &__item:last-child {
      margin-right: 0px;
    }
  }
}

.pb {
  margin-bottom: em(20px);
}
.pb:last-child {
  margin-bottom: em(40px);
  @include ifmobile {
    margin-bottom: em(20px);
  }
}

</style>
