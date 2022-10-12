<template>
  <header-wrapper />
  <main-header />
  <div class="main"></div>
</template>

<script>
import HeaderWrapper from './components/HeaderWrapper.vue'
import MainHeader from './components/MainHeader.vue'

export default {
  name: 'App',
  components: {
    HeaderWrapper,
    MainHeader
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
  .main{
    height: 1000px;
  }
</style>
