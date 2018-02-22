<template>
    <div class="follow">
        <myheader></myheader>
        <div class="content my-container">
            <div class="row">
                <div class="aside">
                    <a class="change-type">全部关注</a>
                    <ul class="js-subscription-list">
                        <li class="router-link-exact-active active">
                            <a href="javascript:void(0)" class="wrap">
                                <div class="avatar">
                                    <img src="../assets/img/addfollow.png" alt="">
                                </div>
                                <div class="name">添加关注</div>
                            </a>
                        </li>
                    </ul>
                </div>
                <div class="main">
                    <div>
                        <ul class="trigger-menu">
                            <nuxt-link active-class="active" tag="li" to="/follow" exact>
                                <a>全部推荐</a>
                            </nuxt-link>
                            <nuxt-link active-class="active" tag="li" to="/follow/authorRecome">
                                <a>
                                    <i class="fa fa-user"></i>
                                    推荐作者
                                </a>
                            </nuxt-link>
                            <nuxt-link active-class="active" tag="li" to="/follow/specialRecome">
                                <a>
                                    <i class="fa fa-th-large"></i>
                                    推荐专题
                                </a>
                            </nuxt-link>
                        </ul>
                        <nuxt-child/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import myheader from '../components/myHeader'
    export default {
        name: "follow",
        components:{
            myheader
        }
    }
</script>

<style scoped>
    .content{
        width: 960px!important;
        margin: 0 auto!important;
        padding: 0 15px;
    }
    .content .row{
        padding: 30px 0;
        margin: 0 -15px;
    }
    .content .row .aside{
        position: fixed;
        top: 0;
        bottom: 0;
        margin: 86px 0 0;
        padding: 0 0 30px;
        width: 280px;
        overflow: auto;
        border-right: 1px solid #f0f0f0;
    }
    .content .row .aside .change-type{
        margin-left: 15px;
        font-size: 15px;
    }
    .content .row .aside ul{
        margin-top: 7px;
        border-top: 1px solid #f0f0f0;
    }
    .content .row .aside ul li{
        line-height: 20px;
    }
    .content .row .aside li.active .wrap {
        display: block;
        background-color: #f0f0f0;
        color: #333;
        border-radius: 0 0 0 4px!important;
        padding: 10px 15px;
    }
    .content .row .aside .avatar {
        width: 40px;
        height: 40px;
        margin-right: 4px;
        display: inline-block;
    }
    .content .row .aside .avatar img {
        width: 100%;
        height: 100%;
        border: 1px solid #ddd;
        border-radius: 50%;
    }
    .content .row .aside .name{
        font-size: 14px;
        vertical-align: middle;
        display: inline-block;
        max-width: 160px;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }
    .content .row .main{
        padding-left: 0;
        margin-left: 33.333%;
        width: 66.66667%;
    }
    .content .row .main div .trigger-menu{
        margin-bottom: 20px;
        border-bottom: 1px solid #f0f0f0;
        font-size: 16px;
        color: #333;
    }
    .content .row .main div .trigger-menu li.active{
        border-bottom: 2px solid #646464!important;
    }
    .content .row .main div .trigger-menu li{
        position: relative;
        display: inline-block;
        padding: 8px 0;
        margin-bottom: -1px;
    }
    .content .row .main div .trigger-menu .active a{
        color: #646464!important;
    }
    .content .row .main div .trigger-menu li a{
        padding: 13px 20px;
        font-size: 15px;
        font-weight: 700;
        color: #969696!important;
        line-height: 25px;
    }
    @media (max-width: 1080px) {
        .content{
            width: 750px!important;
        }
        .aside{
            width: 218.75px;
        }
        .content .row .aside .name{
            max-width: 100px;
        }
    }
    @media (max-width: 750px) {
        .follow{
            overflow: hidden;
        }
    }
</style>