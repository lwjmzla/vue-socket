<template>
  <div id="app">

    <!-- <keep-alive> -->
      <router-view></router-view>
    <!-- </keep-alive> -->

  </div>
</template>

<script>
import Chatting from './components/Chatting/Chatting.vue';
import Login from './components/Login/Login.vue';


export default {
  name: 'app',
  components: {
    Chatting,
    Login,
  },
  beforeCreate() {
    console.log("%c Powered by Zhaohui - microzz.com","background-image:-webkit-gradient( linear, left top,right top, color-stop(0, #00a419),color-stop(0.15, #f44336), color-stop(0.29, #ff4300),color-stop(0.3, #AA00FF),color-stop(0.4, #8BC34A), color-stop(0.45, #607D8B),color-stop(0.6, #4096EE), color-stop(0.75, #D50000),color-stop(0.9, #4096EE), color-stop(1, #FF1A00));color:transparent;-webkit-background-clip:text;font-size:13px;");
  },
  async created() {
    localStorage.addr = '未知';
    
    const sign = 'bb9afbba667fd0deb80ea7faea3f1c5f'
    const infos = await this.axios.get(`http://cp-tools.cn/geo/getPosition?sign=${sign}`)
    const data = infos.data
    if (data.province.length) {
      localStorage.addr = data.province + data.city
    }
  }
}
</script>

<style lang="scss">
@import "./common/style/base.scss";

#app {
  position: relative;
  width: 100%;
  height: 100%;
}
</style>
