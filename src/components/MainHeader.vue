<template>
    <div class="main-header">
        <div class="logo">
            <a href="index.html"><img src="@/assets/Logo/logo.png" alt=""></a>
        </div>
        <div class="search-bar">
            <input type="text" placeholder="Nhập tên sản phẩm, từ khoá cần tìm">
            <div class="btn">
                <i class="ti-search"></i>
            </div>
        </div>
        <div class="right-list">
            <div class="built-pc">
                <div class="img"><img src="../assets/Icon/wrench.png" alt=""></div>
                <div class="text">Xây dựng cấu hình</div>
            </div>
            <div class="built-water-cooling">
                <div class="img"><img src="../assets/Icon/temperature.png" alt=""></div>
                <div class="text">Xây dựng tản nhiệt nước</div>
            </div>
            <div class="cart">
                <img src="../assets/Icon/cart.png" alt="">
                <span>Giỏ hàng</span>
                <div class="in-cart">0</div>
            </div>
        </div>
    </div>
</template>

<style scoped>
    @import url('../assets/Icon/themify-icons/themify-icons.css');
    .main-header{
        background-color: #f4f4f4;
        width: 1180px;
        padding: 20px auto;
        display: flex;
        margin: 0 auto 0;
        padding: 20px 0 20px;
    }
    .logo{
        width: 200px;
    }
    .search-bar{
        flex: 2;
        display: flex;
        border: 2px solid #ed1b24;
        height: 31px;
        margin: auto 5px;
        background-color: #ffffff;
        border-radius: 40px;
    }
    .search-bar>input{
        flex: 9;
        height: 80%;
        margin-left: 20px;
        outline: none;
        border: none;
        padding-top: 10px;
    }
    .search-bar .btn{
        background-color: #ed1b24;
        flex: 1;
        border-radius: 0 40px 40px 0;
        text-align: center;
    }
    .search-bar .ti-search{
        color: white;
        line-height: 26px;
        font-weight: bold;
    }
    .right-list{
        flex: 1;
        display: flex;
        align-items: center;
    }
    .right-list>div{
        display: flex;
    }
    .right-list .img{
        border-radius: 100%;
        width: 34px;
        height: 34px;
        border: 1px solid #b4b4b4;
    }
    .right-list img{
        width: 20px;
        margin: 6px;
    }
    .right-list .built-pc .text{
        font-size: 12px;
        width: 60px;
        margin-left: 5px;
        margin-top: 5px;
    }
    .right-list .built-water-cooling .text{
        font-size: 12px;
        width: 80px;
        margin-left: 5px;
        margin-top: 5px;
    }
    .right-list .cart{
        flex: 1;
        font-size: 12px;
        position: relative;
    }
    .cart img{
        width: 32px;
    }
    .cart span{
        line-height: 44px;
    }
    .cart .in-cart{
        position: absolute;
        background-color: red;
        border: 1px solid white;
        border-radius: 100%;
        width: 16px;
        text-align: center;
        color: white;
        top: 2px;
        left: 20px;
    }
</style>
