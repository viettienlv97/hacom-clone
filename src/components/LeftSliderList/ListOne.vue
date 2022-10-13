<template>
    <div class="container">
        <div class="list-container">
            <div class="list-top">
                <div class="list-first">
                    <a href="" class="a-red">Laptop Theo Hãng</a>
                    <a href="" class="a-underline">Laptop Acer</a>
                    <a href="" class="a-underline">Laptop Asus</a>
                    <a href="" class="a-underline">Laptop Alienware</a>
                    <a href="" class="a-underline">Laptop Dell</a>
                    <a href="" class="a-underline">Laptop HP</a>
                    <a href="" class="a-underline">Laptop Lenovo</a>
                    <a href="" class="a-underline">Laptop Apple</a>
                    <a href="" class="a-underline">Laptop MSI</a>
                    <a href="" class="a-underline">Laptop LG</a>
                    <a href="" class="a-underline">Laptop Gigabyte</a>
                    <a href="" class="a-underline">Laptop Concept D</a>
                    <a href="" class="a-underline">Laptop VGS Imperium</a>
                    <a href="" class="a-underline">Laptop Avita</a>
                    <a href="" class="a-underline">Microsoft Surface</a>
                </div>
                <div class="list-second">
                    <a href="" class="a-red">Laptop Gaming</a>
                    <a href="" class="a-underline">Laptop Acer</a>
                    <a href="" class="a-underline">Laptop Dell</a>
                    <a href="" class="a-underline">Laptop Alienware</a>
                    <a href="" class="a-underline">Laptop HP</a>
                    <a href="" class="a-underline">Laptop Asus</a>
                    <a href="" class="a-underline">Laptop Lenovo</a>
                    <a href="" class="a-underline">Laptop MSI</a>
                    <a href="" class="a-underline">Laptop Gigabyte</a>
                    <a class="a-red">Laptop Theo Nhu Cầu</a>
                    <a href="">Laptop Gaming</a>
                    <a href="">Laptop Đồ Hoạ, Kiến Trúc</a>
                    <a href="">Phổ Thông, Văn Phòng</a>
                    <a href="">Mỏng Nhẹ, Thời Trang</a>
                    <a href="">Laptop Hỗ Trợ Mạng 5G</a>
                </div>
                <div class="list-third">
                    <a class="a-red">Laptop Theo Khoảng Giá</a>
                    <a href="">Dưới 10 Triệu</a>
                    <a href="">10 Triệu - 15 Triệu</a>
                    <a href="">15 Triệu - 20 Triệu</a>
                    <a href="">20 Triệu - 25 Triệu</a>
                    <a href="">25 Triệu - 30 Triệu</a>
                    <a href="">30 Triệu - 35 Triệu</a>
                    <a href="">35 Triệu - 40 Triệu</a>
                    <a href="">40 Triệu - 45 Triệu</a>
                    <a href="">45 Triệu - 50 Triệu</a>
                    <a href="">50 Triệu - 60 Triệu</a>
                    <a href="">60 Triệu - 70 Triệu</a>
                    <a href="">70 Triệu - 80 Triệu</a>
                    <a href="">Trên 80 Triệu</a>
                </div>
                <div class="list-fourth">
                    <a class="a-red">Laptop Theo Cấu Hình</a>
                    <a>CPU</a>
                    <a>VGA</a>
                    <a>RAM</a>
                    <a>Kích Thước Màn Hình</a>
                    <a>Độ Phân Giải Màn Hình</a>
                    <a>Tần Số Màn Hình</a>
                    <a>Cảm Ứng Màn Hình</a>
                    <a>Tuỳ Chọn Ổ Cứng</a>
                    <a>Hệ Điều Hành</a>
                </div>
            </div>
            <div class="list-bottom">
                <div class="list-first">
                    <a href="" class="a-red">Máy Tính Bảng</a>
                    <a href="" class="a-underline">Máy Tính Bảng Apple</a>
                    <a href="" class="a-underline">Máy Tính Bảng Samsung</a>
                    <a href="" class="a-underline">Máy Tính Bảng Lenovo</a>
                </div>
                <div class="list-second">
                    <a href="" class="a-red">Điện Thoại</a>
                    <a href="">Điện Thoại iPhone</a>
                </div>
                <div class="list-third">
                    <a href="" class="a-red">Linh Kiện Laptop</a>
                    <a href="" class="a-red">Phụ Kiện Laptop</a>
                </div>
                <div class="list-fourth">
                    <a href="" class="a-red">Phụ Kiện Surface</a>
                </div>
            </div>
        </div>
        <div class="list-logo">
            <a v-for="item in listLogo" href="" :key="item">
                <img :src="getImgUrl(item)" alt="">
            </a>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      listLogo: [
        'acer',
        'alienware',
        'apple',
        'asus',
        'dell',
        'hp',
        'lenovo',
        'lg',
        'msi',
        'microsoft',
        'gigabyte',
        'fujitsu',
        'vgs',
        'avita'
      ]
    }
  },
  methods: {
    getImgUrl (item) {
      return require('@/assets/logo/brand/' + item + '.png')
    }
  }
}
</script>

<style scoped>
    a{
        text-decoration: none;
        color: #5f686f;
    }
    a:hover{
        color: red;
    }
    a.a-red{
        color: red;
    }
    a.a-underline:hover{
        text-decoration: underline;
    }
    .container{
        position: absolute;
        background-color: #ffffff;
        z-index: 999999;
        width: 980px;
        min-height: 469px;
        top: 0;
        left: 100%;
        border: 1px solid #e1e1e1;
        display: flex;
    }
    .list-container{
        flex: 4;
        display: flex;
        flex-direction: column;
    }
    .list-container a{
        margin: 6px 0 6px 10px;
    }
    .list-top{
        display: flex;
    }
    .list-first,.list-second,.list-third,.list-fourth{
        display: flex;
        flex-direction: column;
        flex: 1;
    }
    .list-bottom{
        display: flex;
    }
    .list-logo{
        flex: 1;
        display: flex;
        flex-wrap: wrap;
        align-content: flex-start;
    }
    .list-logo a{
        width: 45%;
        height: 40px;
        margin-right: 5px;
        margin-top: 5px;
        display: flex;
        background: #eeeeee;
        margin-bottom: 1px;
    }
    .list-logo a img {
        width: 90%;
        margin: auto;
    }
</style>
