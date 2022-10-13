<template>
    <div class="homepage-slider">
        <div class="slider-left">
            <ul
                @mouseover="listShow = true"
                @mouseleave="listShow = false">
                <li
                @mouseover="logger($event, index)"
                v-for="(item,index) in sliderList"
                :key="index"
                >{{item}}
                </li>
                <component
                v-show="listShow"
                :is="currentComponent" />
            </ul>
        </div>
        <div class="slider-container">
            <div class="top-slider">
                <div class="main-slider">
                    <img src="../assets/img/slider-1.jpg" alt="" id="main-img">
                </div>
                <div class="side-slider">
                    <img src="../assets/img/side-img-1.jpg" alt="" class="side-img-1">
                    <img src="../assets/img/side-img-2.jpg" alt="" class="side-img-2">
                </div>
            </div>
            <div class="bottom-slider">
                <img src="../assets/img/main-slide-bot-1.jpg" alt="">
                <img src="../assets/img/main-slide-bot-2.jpg" alt="">
                <img src="../assets/img/bottom-slider-3.jpg" alt="">
            </div>
        </div>
    </div>
</template>

<script>
import ListOne from './LeftSliderList/ListOne.vue'
import ListTwo from './LeftSliderList/ListTwo.vue'
import ListThree from './LeftSliderList/ListThree.vue'
import ListFour from './LeftSliderList/ListFour.vue'
import ListFive from './LeftSliderList/ListFive.vue'
import ListSix from './LeftSliderList/ListSix.vue'
import ListSeven from './LeftSliderList/ListSeven.vue'
import ListEight from './LeftSliderList/ListEight.vue'
import ListNine from './LeftSliderList/ListNine.vue'
import ListTen from './LeftSliderList/ListTen.vue'
import ListEleven from './LeftSliderList/ListEleven.vue'
import ListTwelve from './LeftSliderList/ListTwelve.vue'
import ListThirteen from './LeftSliderList/ListThirteen.vue'
import ListFourteen from './LeftSliderList/ListFourteen.vue'
import ListFifteen from './LeftSliderList/ListFifteen.vue'
import ListSixteen from './LeftSliderList/ListSixteen.vue'
import ListSeventeen from './LeftSliderList/ListSeventeen.vue'
import ListEighteen from './LeftSliderList/ListEighteen.vue'

export default {
  components: {
    // eslint-disable-next-line vue/no-unused-components
    ListOne,
    ListTwo,
    ListThree,
    ListFour,
    ListFive,
    ListSix,
    ListSeven,
    ListEight,
    ListNine,
    ListTen,
    ListEleven,
    ListTwelve,
    ListThirteen,
    ListFourteen,
    ListFifteen,
    ListSixteen,
    ListSeventeen,
    ListEighteen

  },
  data () {
    return {
      sliderList: [
        'Laptop, Tablet, Mobile',
        'Phụ Kiện Laptop, PC, Mobile',
        'PC Gaming, Streaming',
        'Pc Đồ Hoạ, Render, Máy chủ',
        'PC Văn Phòng, AIO, Mini PC',
        'Linh Kiện Máy Tính',
        'Tản Nhiệt PC, Cooling',
        'Màn Hình Máy Tính',
        'Phím Chuột, Ghế Game, Gear',
        'Máy Chơi Game, Tay Game',
        'Loa, Tai Nghe, Mic, Webcam',
        'Camera Quan Sát',
        'Máy In, Máy Chấm Công',
        'Thiết Bị Văn Phòng Khác',
        'TB Siêu Thị, Máy Bán Hàng',
        'Họp, Giảng Dạy, Stream',
        'Thiết Bị Lưu Trữ, USB, Thẻ',
        'Thiết Bị Mạng, Phần Mềm'
      ],
      leftList: [
        'ListOne',
        'ListTwo',
        'ListThree',
        'ListFour',
        'ListFive',
        'ListSix',
        'ListSeven',
        'ListEight',
        'ListNine',
        'ListTen',
        'ListEleven',
        'ListTwelve',
        'ListThirteen',
        'ListFourteen',
        'ListFifteen',
        'ListSixteen',
        'ListSeventeen'
      ],
      currentComponent: '',
      listShow: false
    }
  },
  methods: {
    logger (e, i) {
      switch (i) {
        case 0:
          this.currentComponent = ListOne
          break
        case 1:
          this.currentComponent = ListTwo
          break
        case 2:
          this.currentComponent = ListThree
          break
        case 3:
          this.currentComponent = ListFour
          break
        case 4:
          this.currentComponent = ListFive
          break
        case 5:
          this.currentComponent = ListSix
          break
        case 6:
          this.currentComponent = ListSeven
          break
        case 7:
          this.currentComponent = ListEight
          break
        case 8:
          this.currentComponent = ListNine
          break
        case 9:
          this.currentComponent = ListTen
          break
        case 10:
          this.currentComponent = ListEleven
          break
        case 11:
          this.currentComponent = ListTwelve
          break
        case 12:
          this.currentComponent = ListThirteen
          break
        case 13:
          this.currentComponent = ListFourteen
          break
        case 14:
          this.currentComponent = ListFifteen
          break
        case 15:
          this.currentComponent = ListSixteen
          break
        case 16:
          this.currentComponent = ListSeventeen
          break
        case 17:
          this.currentComponent = ListEighteen
          break
      }
    },
    offListShow () {
    }
  }
}
</script>

<style scoped>
    .homepage-slider{
        width: 1180px;
        display: flex;
        font-size: 11px;
        color: #5f686f;
        margin: 0 auto;
        letter-spacing: 1px;
    }
    .slider-left{
        min-width: 200px;
        position: relative;
    }
    .slider-left>ul{
        list-style: none;
        border: 1px solid #e1e1e1;
        border-radius: 4px;
    }
    .slider-left>ul>li{
        padding: 6.5px 10px;
        border-bottom: 1px solid #e1e1e1;
        background-color: #ffffff;
    }
    .slider-left>ul>li:hover{
        cursor: pointer;
        background-color: #f4f4f4;
    }
    .slider-left>ul>li:last-child{
        border: none !important;
    }
    .slider-container{
        margin-left: 5px;
        display: flex;
        flex-direction: column;
        height: 469px;
        width: 100%;
    }
    .top-slider{
        display: flex;
        flex: 2.1;
        height: 200px;
        margin-bottom: 5px;
    }
    .top-slider .main-slider{
        flex: 2;
        margin-right: 5px;
    }
    .top-slider .main-slider img{
        width: 100%;
        height: 100%;
    }
    .top-slider .side-slider{
        flex: 1;
        display: flex;
        flex-direction: column;
        height: 100%;
    }
    .top-slider .side-slider>img{
        width: 100%;
        flex: 1;
        height: 50%;
    }
    .top-slider .side-slider>img:last-child{
        margin-top: 5px;
    }
    .bottom-slider{
        flex: 1;
        display: flex;
        height: 100px;
    }
    .bottom-slider img{
        flex: 1;
        height: 100%;
        margin: 0 5px 0 0;
        width: 100px;
    }
    .bottom-slider img:last-child{
        margin: 0 !important;
    }
    img{
        border-radius: 4px;
    }
</style>
