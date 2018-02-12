<template>
    <div class="f-index">
        <ul class="add-follow-list">
            <li v-for="(l,i) in listData" :key="i">
                <div>
                    <a class="btn btn-success follow">
                        <i class="fa fa-plus"></i>
                        <span>&nbsp;关注</span>
                    </a>
                    <div class="tag">
                        <i class="fa fa-bookmark"></i>
                        <span>简书推荐标题</span>
                    </div>
                    <a href="javascript:void(0)" class="avatar-collection">
                        <img height="100%" width="100%" :src="l.subscription.source.avatar_url" alt="">
                    </a>
                    <div class="info">
                        <a href="javascript:void(0)" class="name">{{l.subscription.source.title}}</a>
                        <p>{{l.subscription.source.content}}</p>
                        <a href="javascript:void(0)">
                            <i class="fa fa-th-large"></i>
                            <span>
                                {{l.subscription.source.public_notes_count}}篇文章&#x3000;
                                {{l.subscription.source.likes_count}}人关注
                            </span>
                        </a>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    import data from '../../assets/json/follow1.json'
    export default {
        name: "all-recome",
        data(){
            return{
                listData:[]
            }
        },
        mounted(){
            // console.log(data.recommendations.slice(0,10))
            this.listData = data.recommendations.slice(0,10);
        }
    }
</script>

<style scoped>
    .add-follow-list li{
        margin: 0 0 20px;
        padding: 0 0 20px;
        border-bottom: 1px solid #f0f0f0;
    }
    .add-follow-list li div{
        overflow: hidden;
        zoom: 1;
    }
    .add-follow-list li div .follow{
        float: right;
        padding: 8px 0;
        margin-top: 5px;
        width: 100px;
        background-color: #42c02e;
        border-radius: 40px;
        color: #fff!important;
    }
    .add-follow-list li div .tag{
        margin-bottom: 13px;
        font-size: 12px;
        color: #ec6e56;
    }
    .add-follow-list li div .tag i{
        margin-right: 5px;
        font-size: 16px;
    }
    .add-follow-list li div .avatar-collection{
        float: left;
        width: 52px;
        height: 52px;
    }
    .add-follow-list li div .info{
        padding-left: 12px;
        line-height: normal;
        min-height: 50px;
    }
    .add-follow-list li div .info .name{
        margin: 0 0 5px;
        font-size: 15px;
        font-weight: 700;
        color: #333!important;
        display: block;
    }
    .add-follow-list li div .info p{
        margin: 0 0 5px;
        font-size: 12px;
        color: #969696;
    }
    .add-follow-list li div .info a{
        margin: 0 0 5px;
        font-size: 12px;
        color: #969696!important;
    }
    .add-follow-list li div .info i{
        margin-right: 2px;
        font-size: 13px;
        color: #999;
    }
</style>