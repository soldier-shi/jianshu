<template>
  <section class="container">
    <div class="logo" style="height: 100px;text-align: left;padding-top: 50px;">
      <nuxt-link to="/">
        <img height="100%" src="../assets/img/error-logo.png"/>
      </nuxt-link>
    </div>
    <div class="content" v-if="error.statusCode == 404">
      <img class="content-img" width="30%" src="../assets/img/error.jpg" alt="" />
      <h3>您要找的页面可能还在火星</h3>
      <p>可能是因为您的链接地址有误、该文章已经被作者删除或转为私密状态。</p>
    </div>
    <nuxt-link class="button" to="/" v-if="error.statusCode === 404">
      <input type="button" class="btn btn-success" value="回到❥简书首页" />
    </nuxt-link>
  </section>
</template>
<script>
    export default {
        props: ['error']
    }
</script>

<style scoped>
  .container{
    text-align: center;
  }
  .content{
    text-align: center;
  }
  .content h3,p{
    padding-top: 20px;
  }
  .content p{
    color: rgba(0,0,0,.35);
    margin-bottom: 50px;
  }
  @media (max-width: 768px) {
    .logo{
      display: none;
    }
  }
</style>
