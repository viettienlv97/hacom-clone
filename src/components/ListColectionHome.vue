<template>
    <div class="list-colection">
        <div v-for="item in items" :key="item" class="item-colection">
            <span class="item-title" v-html="item.title"></span>
            <div class="item">
                <div class="img-container"><img :src="getImgUrl(item.img)" alt="" class="item-img"></div>
                <div class="item-info">
                    <span class="item-name">{{item.name}}</span>
                    <span
                        class="item-price"
                        v-show="item.price == item.lowestPrice ? false : true"
                        >{{item.price}}đ
                    </span>
                    <span
                        v-show="item.price == item.lowestPrice ? false : true"
                        class="item-discount"
                        >(Tiết kiệm: {{item.discount}}%)
                    </span>
                </div>
            </div>
            <span class="item-lowest-price">{{item.lowestPrice}}đ</span>
            <span class="item-instock yes" v-if="item.inStock">Còn hàng</span>
            <span class="item-instock no" v-else>Liên hệ</span>
            <button class="item-btn">Xem tất cả sản phẩm</button>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      items: {
        pc: {
          title: 'CẤU HÌNH PC KHỦNG VẬT VÃ<br><br>GAME THỦ CHƠI GAME ĐÃ',
          img: 'pc.jpg',
          name: 'PC GAMING HACOM SHARK S08 (I5 12400/B660/16GB RAM/500GB SSD/RTX 3060 TI/700W)',
          price: '29.999.000',
          lowestPrice: '25.999.000',
          inStock: true,
          discount: '13'
        },
        monitor: {
          title: 'MỞ RỘNG MÀN HÌNH LAPTOP<br><br>HÀNG ĐỘC CHỈ CÓ Ở HACOM',
          img: 'monitor.jpg',
          name: 'Bộ 02 màn hình mở rộng cho laptop 15 inch E-Tech S15 - Full HD - MÀU ĐEN',
          price: '9.999.000',
          lowestPrice: '7.999.000',
          inStock: false,
          discount: ''
        },
        allInOne: {
          title: 'TẤT CẢ TRONG MỘT<br><br>ALL IN ONE, MINI PC, LÀ SỐ 1',
          img: 'all-in-one.png',
          name: 'PC Dell Optiplex All in One 3280 (i3-10105T/8GB RAM/256 SSD/21.5 inch FHD/WL+BT/K+M/Ubuntu)',
          price: '17.949.000',
          lowestPrice: '15.699.000',
          inStock: true,
          discount: ''
        },
        waterCooler: {
          title: 'XƯỞNG ĐỘ PC CHUYÊN NGHIỆP<br><br>NƠI RA LÒ CÁC SIÊU PHẨM',
          img: 'water-cooler.jpg',
          name: 'Trọn bộ tản nhiệt nước PC THERMALTAKE VIEW71 (Lắp ráp theo yêu cầu)',
          price: '66.951.000',
          lowestPrice: '66.951.000',
          inStock: true,
          discount: ''
        }
      }
    }
  },
  methods: {
    getImgUrl (img) {
      return require('../assets/img/colections/' + img)
    },
    discountCal (one) {
      console.log(one)
    }
  }
}
</script>

<style scoped>
    .list-colection{
        width: 1180px;
        margin: 0 auto 0;
        display: flex;
        padding: 20px 15px 0;
        background-color: #ffffff;
    }
    .item-colection{
        width: 25%;
        display: flex;
        flex-direction: column;
        height: 500px;
    }
    .item-title{
        text-align: center;
        font-size: 16px;
        color: #d82a29;
        justify-items: center;
        margin: 0 10px;
        font-weight: 400;
        display: block;
        height: 60px;
    }
    .item{
        width: 258px;
        margin: 0 auto;
        display: flex;
        flex-direction: column;
    }
    .img-container{
        height: 216px;
        text-align: center;
        margin-bottom: 36px;
        display: flex;
    }
    .img-container>img{
        width: 206px;
        margin: auto;
    }
    .item-info{
        font-size: 12px;
    }
    .item-info .item-name{
        display: block;
        margin-bottom: 12px;
    }
    .item-info .item-price{
        text-decoration: line-through;
        font-size: 15px;
        color: rgb(105, 105, 105);
    }
    .item-info .item-discount{
        color: #d82a29;
        margin-left: 10px;
    }
    .item-lowest-price{
        width: 258px;
        display: block;
        font-size: 20px;
        font-weight: 700;
        justify-self: end;
        margin: auto auto 10px;
    }
    .item-instock{
        justify-self: end;
        width: 258px;
        font-size: 14px;
        margin: 0 auto 20px;
    }
    .item-instock.yes{
        color: green;
    }
    .item-instock.no{
        color: blue;
    }
    .item-btn{
        justify-self: end;
        margin: 0 18px 20px;
        height: 36px;
        background-color: #243a76;
        color: white;
        font-weight: 200;
        font-size: 12px;
        border: none;
        border-radius: 4px;
    }
</style>
