<template>
    <div class="homepage-slider">
        <div class="slider-left">
            <ul>
                <li @click="logger($event, index)" v-for="(item,index) in sliderList" :key="index">{{item}}</li>
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
export default {
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
      ]
    }
  },
  methods: {
    logger (e, i) {
      console.log(i)
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
