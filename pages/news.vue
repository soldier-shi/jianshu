<template>
    <div class="news-container">
        <myheader></myheader>
        <div class="content my-container">
            <div class="row">
                <div class="aside">
                    <ul>
                        <li>
                            <nuxt-link active-class="active" to="/news" exact>
                                <i class="fa fa-comment-o"></i>
                                <span>评论</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link active-class="active" to="/news/message">
                                <i class="fa fa-envelope-open-o"></i>
                                <span>简信</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link active-class="active" to="/news/request">
                                <i class="fa fa-upload"></i>
                                <span>投稿请求</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link active-class="active" to="/news/like">
                                <i class="fa fa-heart-o"></i>
                                <span>喜欢和赞</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link active-class="active" to="/news/follow">
                                <i class="fa fa-user-o"></i>
                                <span>关注</span>
                            </nuxt-link>
                        </li>
                    </ul>
                </div>
                <nuxt-child/>
            </div>
        </div>
    </div>
</template>

<script>
    import myheader from '../components/myHeader'
    export default {
        name: "news",
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
    }
    .content .row .aside ul{
        margin-top: 0;
        margin-bottom: 10px;
    }
    .content .row .aside ul li{
        line-height: 20px;
        margin: 0;
        color: #333;
    }
    .content .row .aside ul li a{
        height: auto;
        padding: 10px 25px;
        line-height: 30px;
        display: block;
        background-color: transparent;
    }
    .content .row .aside ul li a i{
        margin-right: 15px;
        font-size: 24px;
        color: #ea6f5a;
        vertical-align: middle;
    }
    .content .row .aside ul li a span{
        font-size: 15px;
        vertical-align: middle;
    }
    .content .row .aside ul li a.active {
        background-color: #f0f0f0;
        border-radius: 4px;
    }

    @media (max-width: 1080px) {
        .content{
            width: 750px!important;
        }
        .aside{
            width: 218.75px!important;
        }
    }
    @media (max-width: 750px) {
        .news-container{
            overflow: hidden;
        }
    }
</style>