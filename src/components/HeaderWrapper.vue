<template>
    <div class="container-wrapper">
        <div class="container">
        <div class="container-left">
            <div class="line-call" @mouseover="lineCallShow = true" @mouseleave="lineCallShow = false">
                <img src="../assets/Icon/phone.png" alt="" style="width: 11px">
                Gọi mua hàng:
                <span>1900.1903</span>
                <ul class="line-call-list" v-show="lineCallShow">
                    <li><span>Line 1</span>Mua hàng trực tuyến (8h - 24h)</li>
                    <li><span>Line 2</span>Hỗ trợ kỹ thuật (9h - 21h30)</li>
                    <li><span>Line 3</span>Dịch vụ kỹ thuật - bảo hành (9h - 17h30)</li>
                    <li><span>Line 0</span>Chăm sóc khách hàng (8h - 21h30)</li>
                </ul>
            </div>
            <div class="personal-customer">
                <span>Khách cá nhân</span>
            </div>
            <div class="company-customer">
                <span>Khách doanh nghiệp</span>
                <div class="company-customer-wrapper"></div>
            </div>
            <div class="sale-of-hcm">
                <span>Bán hàng - TP HCM</span>
                <div class="sale-of-hcm-wrapper"></div>
            </div>
        </div>
        <header-container-right />
        </div>
    </div>
    <div class="wrapper" v-show="wrapperShow"></div>
</template>

<script>
// import PersonalCustomerSupport from './PersonalCustomerSupport.vue'
import HeaderContainerRight from './HeaderContainerRight.vue'

export default {
  data () {
    return {
      lineCallShow: false,
      perCustomerShow: false,
      wrapperShow: false
    }
  },
  components: {
    // PersonalCustomerSupport
    HeaderContainerRight
  },
  methods: {
    showWrapper () {
      this.wrapperShow = true
    },
    hideWrapper () {
      this.wrapperShow = false
    }
  }
}
</script>

<style scoped>
    .container-wrapper{
        width: 100%;
        height: 37px;
        border-bottom: 1px solid #ccc;
        font-size: 11px;
        align-items: center;
    }
    .container{
        max-width: 1180px;
        height: 100%;
        display: flex;
        margin: 0 auto 0 auto;
        justify-content: space-between;

    }
    .container-left{
        display: flex;
        align-items: center;
    }
    .container-left .line-call,
    .container-left .personal-customer,
    .container-left .company-customer,
    .container-left .sale-of-hcm{
        position: relative;
        color: #333e48;
        margin-right: 10px;
        display: block;
        text-align: center;
        height: 30px;
    }
    .container-left .line-call{
        height: 100%;
        line-height: 37px;
    }
    .container-left .line-call:hover{
        cursor: pointer;
    }
    .container-left .line-call>span{
        font-weight: bold;
    }
    .container-left .line-call ul{
        position: absolute;
        list-style: none;
        border: 1px solid black;
        border-top: none;
        border-bottom: none;
        width: 280px;
        border-radius: 3px;
        z-index: 1;
        background-color: #ffffff;
    }
    .container-left .line-call li{
        border-bottom: 1px solid black;
    }
    .line-call li span {
        color: white;
        border-radius: 3px;
        background-color: #233974;
        padding: 3px 8px;
        margin:0 8px;
    }
    .personal-customer,
    .company-customer,
    .sale-of-hcm{
        text-align: center;
        padding: 0 20px;
        border-radius: 20px;
        background-image: linear-gradient(90deg, blue, red);
        z-index: 1;
    }
    .personal-customer:hover,
    .company-customer:hover,
    .sale-of-hcm:hover{
        cursor: pointer;
    }
    .personal-customer>span,
    .company-customer>span,
    .sale-of-hcm>span{
        line-height: 30px;
        color: white;
    }

    .wrapper{
        position: relative;
        top: -50px;
        width: 100%;
        height: 100vh;
        background-color: rgba(0, 0, 0, 0.2);
    }
</style>
