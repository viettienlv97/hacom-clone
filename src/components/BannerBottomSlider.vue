<template>
    <div class="banner-bottom">
        <img v-for="pic in pics" :key="pic" :src="getImgUrl(pic)" alt="">
    </div>
</template>

<script>
export default {
  data () {
    return {
      pics: [
        'banner-0',
        'banner-1',
        'banner-2',
        'banner-3'
      ]
    }
  },
  methods: {
    getImgUrl (pic) {
      return require('../assets/img/' + pic + '.jpg')
    }
  }
}
</script>

<style scoped>
    .banner-bottom{
        width: 1180px;
        margin: 5px auto;
        display: flex;
    }
    .banner-bottom>img{
        width: 100px;
        flex: 1;
        margin-right: 5px;
    }
    .banner-bottom>img:last-child{
        margin: 0;
    }
</style>
