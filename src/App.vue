<template>
  <header-wrapper />
</template>

<script>
import HeaderWrapper from './components/HeaderWrapper.vue'

export default {
  name: 'App',
  components: {
    HeaderWrapper
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
</style>
