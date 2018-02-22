<template>
    <div class="likeArticle">
    	<myheader></myheader>
        <div class="my-container person">
            <div class="row">
                <div class="col-8 main">
                    <div class="main-top">
                        <a class="avatar" href="javascript:void(0)">
                            <img src="../assets/img/default-avatar.jpg" alt="">
                        </a>
                        <div class="title">
                            <a class="name" href="javascript:void(0)">啦啦啦</a>
                        </div>
                        <div class="info">
                            <ul>
                                <li>
                                    <div class="meta-block">
                                        <a href="javascript:void(0)"></a>
                                        <p>0</p>
                                        <span>关注</span>
                                        <i class="fa fa-angle-right"></i>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <a href="javascript:void(0)"></a>
                                        <p>0</p>
                                        <span>粉丝</span>
                                        <i class="fa fa-angle-right"></i>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <a href="javascript:void(0)"></a>
                                        <p>0</p>
                                        <span>文章</span>
                                        <i class="fa fa-angle-right"></i>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <p>0</p>
                                        <div>字数</div>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block boderll">
                                        <p>0</p>
                                        <div>收获喜欢</div>
                                    </div>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="outer-container">
                        <ul class="triggar-menu">
                            <li>
                                <nuxt-link to="/likeArticle/other" active-class="active">
                                    <span>我关注的专题/文集/连载&nbsp;0</span>
                                </nuxt-link>
                            </li>
                            <li>
                                <nuxt-link to="/likeArticle" active-class="active" exact>
                                    <span>我喜欢的文章&nbsp;0</span>
                                </nuxt-link>
                            </li>
                        </ul>
                        <nuxt-child/>
                    </div>
                </div>
                <div class="col-3.5 aside">
                    <div class="description"></div>
                    <div class="user-publications"></div>
                    <div class="user-courses"></div>
                    <ul class="list user-dynamic">
                    	<li>
                    		<nuxt-link to="/asasasas">
                    			<i class="fa fa-th-large"></i>
                    			<span>我关注的专题/文集/连载</span>
                    		</nuxt-link>
                    	</li>
                    	<li>
                    		<nuxt-link to="asasqwqw">
                    			<i class="fa fa-heart-o"></i>
                    			<span>我喜欢的文章</span>
                    		</nuxt-link>
                    	</li>
                    </ul>
                    <div>
                    	<div>
                    		<div class="title">我创建的专题</div>
                    		<div class="new-collection-block">
                    			<nuxt-link to="/asaswww">
                    				<i class="fa fa-plus"></i>
                    				<span>创建一个新专题</span>
                    			</nuxt-link>
                    		</div>
                    	</div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
	import myheader from '../components/myHeader'
    export default {
        name: "like-article",
        components:{
        	myheader
        }
    }
</script>

<style scoped>
    .likeArticle .person .row{
        padding-top: 30px;
    }
    .likeArticle .person .row .main{
        padding-right: 0;
    }
    .likeArticle .person .row .main .main-top{
        margin-bottom: 20px;
        overflow: hidden;
        zoom: 1;
    }
    .likeArticle .person .row .main .main-top .avatar{
        width: 80px;
        height: 80px;
        float: left;
    }
    .likeArticle .person .row .main .main-top .title{
        padding: 5px 0 0 100px;
    }
    .likeArticle .person .row .main .main-top .title .name{
        display: inline;
        font-size: 21px;
        font-weight: 700;
        vertical-align: center;
    }
    .likeArticle .person .row .main .main-top .info{
        margin-top: 5px;
        padding-left: 100px;
        font-size: 14px;
    }
    .info ul li{
        display: inline-block;
    }
    .person .main .main-top .info ul .meta-block {
        font-size: 12px;
        margin: 0 7px 6px 0;
        padding: 0 7px 0 0;
        border-right: 1px solid #f0f0f0;
        color: #969696!important;
    }
    .person .main .main-top .info ul .meta-block a{
        color: #969696;
    }
    .person .main .main-top .info ul p {
        margin-bottom: -3px;
        font-size: 15px;
        color: #333;
    }
    .person .main .main-top .info ul span{
        margin-right: 5px;
    }
    .boderll{
        border: none!important;
    }
    .likeArticle .person .row .main .outer-container .triggar-menu{
    	margin-bottom: 20px;
    	border-bottom: 1px solid #F0F0F0;
    	padding-bottom: 5px;
    }
    .triggar-menu li{
    	position: relative;
	    display: inline-block;
	    padding: 8px 0;
	    margin-bottom: -1px;
    }
    .triggar-menu li a{
    	padding: 13px 20px;
	    font-size: 15px;
	    font-weight: 700;
	    color: #969696!important;
	    line-height: 25px;
    }
    .triggar-menu li a.active{
    	border-bottom: 2px solid #646464;
    }
    .triggar-menu li a i{
    	margin-right: 5px;
    	font-size: 17px;
    }
    .likeArticle .person .row .aside{
    	margin-left: 3.166667%;
    }
    .likeArticle .person .row .aside .description{
    	position: relative;
	    margin-bottom: 16px;
	    padding: 0 0 16px;
	    text-align: left;
	    font-size: 0;
	    border-bottom: 1px solid #f0f0f0;
	    clear: both;
	    word-break: break-word!important;
    }
    .likeArticle .person .row .aside .list{
    	margin-bottom: 16px;
	    padding-bottom: 16px;
	    list-style: none;
	    border-bottom: 1px solid #f0f0f0;
	    clear: both;
    }
    .likeArticle .person .row .aside .list li{
    	margin-bottom: 10px;
    }
    .likeArticle .person .row .aside .list a{
	    font-size: 14px;
	    color: rgba(0,0,0,.75)!important;
	    line-height: 30px;
	}
	.aside .list a i{
		margin-right: 10px;
	    font-size: 20px;
	    vertical-align: middle;
	}
	.aside .title{
		float: left;
	    margin-bottom: 10px;
	    font-size: 14px;
	    color: #969696;
	}
	.aside .new-collection-block {
	    position: relative;
	    margin-bottom: 16px;
	    padding: 0 0 16px;
	    text-align: left;
	    border-bottom: 1px solid #f0f0f0;
	    clear: both;
	    word-break: break-word!important;
	    word-break: break-all;
	}
	.aside .new-collection-block a{
		margin-right: 5px;
		font-size: 13px;
		color: #42c02e!important;
	}
	.aside .new-collection-block a i{
		margin-right: 2px;
	}
    @media (max-width: 1080px) {
        .myhome .person{
            width: 750px!important;
        }
    }
    @media (max-width: 750px) {
        .myhome{
            overflow: hidden;
        }
    }
</style>