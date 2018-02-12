<template>
    <div class="main">
        <div>
            <div class="menu">全部简信</div>
        </div>
        <ul class="comment-list">
        <div></div>
    </ul>
        <div class="find-nothing">
            <img width="100px" src="../../assets/img/news1.png" alt="">
        </div>
    </div>
</template>

<script>
    export default {
        name: "message"
    }
</script>

<style scoped>
    .main .menu{
        margin-bottom: 20px;
        font-size: 14px;
        font-weight: 700;
    }
    .main .find-nothing{
        margin-top: 150px;
        text-align: center;
    }
    .content .row .main{
        padding-left: 0;
        margin-left: 33.333%;
        width: 66.66667%;
    }
</style>