<template>
    <div class="f-authorRecome">
        <ul class="add-follow-list">
            <li v-for="(l,i) in listData" :key="i">
                <div>
                    <a class="btn btn-success follow">
                        <i class="fa fa-plus"></i>
                        <span>&nbsp;关注</span>
                    </a>
                    <a href="javascript:void(0)" class="avatar-collection">
                        <img height="100%" width="100%" :src="l.subscription.source.avatar_source" alt="">
                    </a>
                    <div class="info">
                        <a href="javascript:void(0)" class="name">{{l.subscription.source.nickname}}</a>
                        <p>{{l.subscription.source.intro}}</p>
                        <a href="javascript:void(0)">
                            <i class="fa fa-file-text"></i>
                            <span>
                                {{l.subscription.source.recent_notes[0].title}}
                            </span>
                        </a>
                        <a href="javascript:void(0)">
                            <i class="fa fa-file-text"></i>
                            <span>
                                {{l.subscription.source.recent_notes[1].title}}
                            </span>
                        </a>
                    </div>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
    import data from '../../assets/json/follow2.json'
    export default {
        name: "author-recome",
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
        margin-right: 10px;
    }
    .add-follow-list li div .info i{
        font-size: 12px;
        color: #999;
    }
</style>