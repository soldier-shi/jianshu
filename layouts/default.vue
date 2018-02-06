<template>
  <div id="default-template">
    <nuxt/>
  </div>
</template>
<script>
import Vue from 'vue'
import BootstrapVue from 'bootstrap-vue'
Vue.use(BootstrapVue)
import 'bootstrap/dist/css/bootstrap.css'
import 'bootstrap-vue/dist/bootstrap-vue.css'
Vue.filter('formatDate',function(value){
  let time = new Date(value);
  let year = time.getFullYear();
  let month = time.getMonth() + 1;
  let date = time.getDate();
  let hour = time.getHours();
  let minute = time.getMinutes();
  let second = time.getSeconds();
  function niceTime(num){
    return num > 10 ? num : '0' + num
  }
  return niceTime(year) + '-' + niceTime(month) + '-' + niceTime(date) + ' | ' + 
          niceTime(hour) + ':' + niceTime(minute) + ':' + niceTime(second)
})
export default {

}
</script>
