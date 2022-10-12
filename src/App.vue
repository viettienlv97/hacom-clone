<template>
  <header-wrapper />
  <main-header />
  <homepage-slider />
  <banner-bottom-slider />
  <div class="main"></div>
</template>

<script>
import HeaderWrapper from './components/HeaderWrapper.vue'
import MainHeader from './components/MainHeader.vue'
import HomepageSlider from './components/HomepageSlider.vue'
import BannerBottomSlider from './components/BannerBottomSlider.vue'

export default {
  name: 'App',
  components: {
    HeaderWrapper,
    MainHeader,
    HomepageSlider,
    BannerBottomSlider
  }
}
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Open+Sans:wght@300&display=swap');
  *{
    font-family: 'Open-sans',sans-serif;
    margin: 0px;
    padding: 0px;
    box-sizing: border-box;
  }
  body{
    background-color: #f4f4f4
  }
  .main{
    height: 1000px;
  }
</style>
