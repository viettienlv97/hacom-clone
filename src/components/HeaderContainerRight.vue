<template>
    <div class="container-right">
        <div class="find-location">
            <span>Tìm cửa hàng gần nhất</span></div>
        <div class="support" @mouseenter="supportShow = true" @mouseleave="supportShow = false">
            <span>Hỗ trợ</span>
            <ul v-show="supportShow" class="support-list">
                <li>Chính sách, quy định chung</li>
                <li>Giao hàng 2h - HACOM Faster</li>
                <li>Chính sách bảo hành</li>
                <li>Chính sách cho doanh nghiệp</li>
                <li>Chính sách hàng chính hãng</li>
                <li>Chính sách nhập lại tính phí</li>
                <li>Hướng dẫn mua hàng trực tuyến</li>
                <li>Hướng dẫn thanh toán</li>
                <li class="last">Hướng dẫn mua hàng trả góp</li>
            </ul>
        </div>
        <div class="service" @mouseenter="serviceShow=true" @mouseleave="serviceShow=false">
            <span>Trung tâm dịch vụ</span>
            <ul v-show="serviceShow">
                <li>Tra cứu bảo hành</li>
                <li>In hoá đơn điện tử</li>
                <li>Gửi yêu cầu bảo hành</li>
                <li class="last">Góp ý, khiếu nại</li>
            </ul>
        </div>
        <div class="promotion"><span>Khuyến mại</span></div>
        <div class="account" @mouseenter="accountListShow = true" @mouseleave="accountListShow = false">
            <span>Tài khoản</span>
            <ul class="account-list" v-show="accountListShow">
                <li class="sign-in">Đăng nhập</li>
                <li class="sign-up">Đăng ký</li>
                <li class="google">Đăng nhập bằng Google</li>
                <li class="facebook">Đăng nhập bằng Facebook</li>
                <li class="zalo">Đăng nhập bằng Zalo</li>
            </ul>
        </div>
    </div>
</template>

<script>
export default {
  data () {
    return {
      supportShow: false,
      serviceShow: false,
      accountListShow: false
    }
  }
}
</script>

<style scoped>
    ul{
        position: absolute;
        list-style: none;
        border: 1px solid #ccc;
        border-radius: 4px;
        background-color: #ffffff;
    }
    .container-right{
        display: flex;
        color: #333e48;
    }
    .container-right>div{
        margin-left: 20px;
        position: relative;
    }
    .container-right>div:hover{
        cursor: pointer;
    }
    .container-right>div>span {
        line-height: 37px;
    }
    .support>ul {
        left: -50px;
        width: 230px;
        font-size: 13px;
    }
    .support>ul>li{
        border-bottom: 1px solid #ccc;
        padding: 10px 0;
        margin: 0 16px;
    }
    .last{
        border: none !important;
        margin-bottom: 4px;
    }
    .service>ul{
        width: 170px;
        left: -30px;
        font-size: 13px;
    }
    .service>ul>li{
        border-bottom: 1px solid #ccc;
        padding: 10px 0;
        margin: 0 16px;
    }
    .account-list{
        width: 220px;
        right: 0;
        padding: 16px;
    }
    .account-list>li{
        font-size: 12px;
        font-weight: bold;
        width: 100%;
        text-align: center;
        padding: 10px 0;
        border-radius: 4px;
        margin-bottom: 5px;
    }
    .sign-in,.sign-up{
        background-color: #fdd835;
        color: #5f5f44;
    }
    .google{
        color: #ffffff;
        background-color: #df4a32;
    }
    .facebook{
        color: #ffffff;
        background-color: #3b5998;
    }
    .zalo{
        color: #ffffff;
        background-color: #0573FF;
    }
</style>
