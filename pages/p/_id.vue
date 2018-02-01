<template>
    <div>
        <my-header></my-header>
        <div class="note">
            <!--文章区域-->
            <div class="post">
                <!--正文-->
                <div class="article">
                    <h1 class="title">月薪三千,就该去死吗？</h1>
                    <div class="author">
                        <nuxt-link class="avatar" to="/u/123">
                            <img src="../../assets/img/pic.jpg" alt="">
                        </nuxt-link>
                        <div class="info">
                            <span class="name">测试用户</span>
                            <a href="javascript:void(0)" class="btn btn-success"
                               @click="order" ref="orders" v-bind:class="{follow:isActive,order:has}"
                               @mouseover="goin" @mouseleave="exit">
                                <i class="fa fa-plus-square-o"></i>
                                关注
                            </a>
                            <div class="meta">
                                <span>2018.01.23 16:09</span>
                                <span>字数 2273</span>
                                <span>阅读 888</span>
                                <span>评论 7</span>
                                <span>喜欢 33</span>
                            </div>
                        </div>
                    </div>
                    <!--文章-->
                    <div class="show-content">
                        <p>
                            可能是春节快要到了，游子回家的旋律吹响，一年一度的“比头疼大赛”又要拉开
                            大幕。比什么？比工作，比资产，比儿女，比婚姻。都市人携带着远方不为所
                            知的辛苦，在同学相聚时，多了些虚伪；在朋友重逢时，少了些真诚。
                        </p>
                        <p>
                            家乡是个让人又爱又恨的地方。有时，常看见有人自嘲：在外大老板，回乡二胖子；
                            在外大哥大，回镇三孙子；在外大名媛，回村小豆子；在外喜当爹，回家好多爹——亲
                            爹不倒，干爹飘飘。
                        </p>
                    </div>
                    <!--文脚-->
                    <div class="show-foot">
                        <nuxt-link to="/nb/123" class="notebook">
                            <i class="fa fa-book"></i>
                            <span>我的文集</span>
                        </nuxt-link>
                        <div class="copyright">
                            © 著作权归作者所有
                        </div>
                    </div>
                    <!--文章底部作者信息-->
                    <div class="follow-detail">
                        <div class="info">
                            <nuxt-link to="/u/123" class="avatar">
                                <img src="../../assets/img/default-avatar.jpg" alt="">
                            </nuxt-link>
                            <a href="javascript:void(0)" class="btn btn-success"
                               @click="order" ref="order" v-bind:class="{follow:isActive,order:has}"
                               @mouseover="goin" @mouseleave="exit">
                                <i class="fa fa-plus-square-o"></i>
                                关注
                            </a>
                            <nuxt-link class="title" to="/u/123">
                                美滋滋
                            </nuxt-link>
                            <i class="fa fa-mars"></i>
                            <p>
                                写了 46873 字，被 26 人关注，获得了 95 个喜欢
                            </p>
                        </div>
                        <div class="signature">
                            为城市里的不安和孤寂发声。

                            微信公众号：得及
                        </div>
                    </div>
                    <div class="meta-bottom">
                        <div class="like">
                            <div class="btn like-group" ref="likeBtn"
                                 :class="{likebtn:likeBtn,likeGroupHover:likeBtnHover}">
                                <div @click="changeBtnlike" class="btn-like" :class="{likeBtnChild:likeBtn}">
                                    <a href="javascript:void(0)">
                                        <i class="fa fa-heart-o"></i>
                                        喜欢
                                    </a>
                                </div>
                                <div class="modal-wrap" :class="{likeBtnChild:likeBtn}">
                                    |<a ref="likeNum">{{likeNum}}</a>
                                </div>
                            </div>
                        </div>
                        <div class="share-group">
                            <transition name="fade">
                                <div class="wxModal" v-show="wxShow">
                                    <div class="box">
                                        分享到微信
                                    </div>
                                </div>
                            </transition>
                            <a href="javascript:void(0)" @mouseover="wxShow = true" @mouseleave="wxShow = false">
                                <i class="fa fa-weixin weixin"></i>
                            </a>
                            <transition name="fade">
                                <div class="wbModal" v-show="wbShow">
                                    <div class="box">
                                        分享到微博
                                    </div>
                                </div>
                            </transition>
                            <a href="javascript:void(0)" @mouseover="wbShow = true" @mouseleave="wbShow = false">
                                <i class="fa fa-weibo weibo"></i>
                            </a>
                            <transition name="fade">
                                <div class="imModal" v-show="imShow">
                                    <div class="box box3">
                                        下载长微博图片
                                    </div>
                                </div>
                            </transition>
                            <a href="javascript:void(0)" @mouseover="imShow = true" @mouseleave="imShow = false">
                                <i class="fa fa-picture-o imgimg"></i>
                            </a>
                            <transition name="fade">
                                <div class="moreModal" v-show="moreShow">
                                    <div class="box4">
                                        <ul>
                                            <li>
                                                <nuxt-link to="/nb/555" style="color: black!important;">
                                                    <i class="fa fa-star" style="color: yellow!important;"></i>
                                                    <span>分享到QQ空间</span>
                                                </nuxt-link>
                                            </li>
                                            <li>
                                                <nuxt-link to="/nb/555" style="color: black!important;">
                                                    <i class="fa fa-twitter" style="color: blue!important;"></i>
                                                    <span>分享到Twitter</span>
                                                </nuxt-link>
                                            </li>
                                            <li>
                                                <nuxt-link to="/nb/555" style="color: black!important;">
                                                    <i class="fa fa-facebook" style="color: darkblue!important;"></i>
                                                    <span>分享到FaceBook</span>
                                                </nuxt-link>
                                            </li>
                                            <li>
                                                <nuxt-link to="/nb/555" style="color: black!important;">
                                                    <i class="fa fa-google" style="color: red!important;"></i>
                                                    <span>分享到Google+</span>
                                                </nuxt-link>
                                            </li>
                                            <li>
                                                <nuxt-link to="/nb/555" style="color: black!important;">
                                                    <i class="fa fa-leaf" style="color: green!important;"></i>
                                                    <span>分享到豆瓣&#x3000;&#x3000;</span>
                                                </nuxt-link>
                                            </li>
                                        </ul>
                                    </div>
                                </div>
                            </transition>
                            <a href="javascript:void(0)" @focus="moreShow = true" @blur="moreShow = false" style="color: rgba(0,0,0,.35)!important;">
                                更多分享
                            </a>
                        </div>
                    </div>
                    <!--评论区-->
                    <div></div>
                </div>
            </div>
            <!--悬浮的操作框-->
            <div class="side-bar"></div>
            <!--对应的推荐阅读-->
            <div class="note-bottom"></div>
        </div>
    </div>
</template>

<script>
    import myHeader from '~/components/myHeader'
    export default {
        components:{
            myHeader
        },
        data(){
            return{
                isActive:true,
                has:false,
                likeBtn:false,
                likeBtnHover:true,
                likeNum:55,
                wxShow:false,
                wbShow:false,
                imShow:false,
                moreShow:false
            }
        },
        watch:{
            likeNum(newlikeNum,oldlikeNum){
                console.log(newlikeNum)
                console.log(oldlikeNum)
            }
        },
        methods:{
            order:function () {

                if(this.isActive == true){
                    this.$refs.orders.innerHTML = `<i class="fa fa-check"></i> 已关注`
                    this.$refs.order.innerHTML = `<i class="fa fa-check"></i> 已关注`
                    this.isActive = !this.isActive;
                    this.has = !this.has;
                }else{
                    this.$refs.orders.innerHTML = ` <i class="fa fa-plus-square-o"></i> 关注`
                    this.$refs.order.innerHTML = ` <i class="fa fa-plus-square-o"></i> 关注`
                    this.isActive = !this.isActive;
                    this.has = !this.has;
                }
            },
            goin: function(){
                if(this.isActive == false){
                    this.$refs.orders.innerHTML = `<i class="fa fa-close"></i> 取消关注`
                    this.$refs.order.innerHTML = `<i class="fa fa-close"></i> 取消关注`
                }
            },
            exit:function () {
                if( this.isActive == false){
                    this.$refs.orders.innerHTML = `<i class="fa fa-check"></i> 已关注`
                    this.$refs.order.innerHTML = `<i class="fa fa-check"></i> 已关注`
                }
            },
            changeBtnlike(){
                if(this.likeBtn == false){
                    this.likeBtn = true;
                    this.likeBtnHover = false;
                    this.$refs.likeNum.innerHTML= this.likeNum + 1
                }else{
                    this.likeBtn = false;
                    this.likeBtnHover = true;
                    this.$refs.likeNum.innerHTML= this.likeNum
                }
            }
        }
    }
</script>

<style scoped>
    .order{
        background: white!important;
        color:grey!important;
        font-size: 12px;
        border-radius: 20px;
        padding: 1px 8px 1px 6px;
        border-color: #7f828b!important;
    }
    .likebtn{
        background-color: #ea6f5a;
    }
    .likeBtnChild{
        color: white!important;
    }
    .fade-enter,.fade-leave-to{
        opacity: 0;
    }
    .fade-enter-active,.fade-leave-active{
        transition: all .3s;
    }
</style>
