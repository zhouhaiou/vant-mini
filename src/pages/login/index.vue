<template>
  <div>
    <div class="login-title">CS一下</div>
    <van-cell-group>
      <van-field
        :value="username"
        required
        clearable
        label="用户名"
        icon="question-o"
        placeholder="请输入用户名"
        v-model="username"
      />

      <input type="text">

      <van-field
        :value="password"
        type="password"
        clearable
        label="密码"
        placeholder="请输入密码"
        required
        :border="false"
      />
    </van-cell-group>

    <a href="/pages/index" class="btn-box">
      <van-button custom-class="aaa" type="primary" size="large">登录</van-button>
    </a>

    <van-button @click="getInputData">获取输入框的值</van-button>

    <van-button @click="showToast">文字提示</van-button>
    <van-button @click="showToast1">文字提示</van-button>
    <van-button @click="showToast2">文字提示mask</van-button>
    <van-button @click="showToast3">文字提示</van-button>

    <van-toast id="van-toast"/>
  </div>
</template>

<script>
import Toast from 'vant-weapp/dist/toast/toast';

export default {
  config: {
    navigationBarTitleText: "登录",
    navigationBarBackgroundColor: "#f40"
  },
  data() {
    return {
      username: "",
      password: ""
    };
  },
  methods: {
    getInputData(){
      console.log('username',this.username)
    },
    showToast(){
      console.log(this);
      Toast('111111')
      // this.$router.push('/pages/list/index')
      // mpvue.navigateTo({url:'/pages/list/index'})
    },
    showToast1(){
      Toast('2222')
    },
    showToast2(){
      Toast({
        message: 'mask',
        mask: true
      })
    },
    showToast3(){
      Toast('2224')
    }
  }

};
</script>

<style lang="scss">
.login-title {
  margin: 20px;
  text-align: center;
  font-size: 20px;
}
</style>
