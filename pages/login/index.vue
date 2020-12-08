<template>
  <view class="login">
    <view class="bg-login-box">
      <image mode="" class="bg-login-img" src="/static/login/bg-login.jpg"></image>
    </view>


    <view class="login-body">
      <view class="title text-white text-xl text-center">
        喂！还不快来玩一下！
      </view>

      <view class="tab">
        <view class="tab-box flex justify-between">
          <view :class="[
          'cu-tag', 'round', 
          'padding-lr-lg', 
          tab == 0 ?  'color-title' : 'text-white',
          tab == 0 ? '' : 'background-none']" @click="handleClickTab(0)">登录</view>
          <view :class="[
          'cu-tag', 'round', 
          'padding-lr-lg', 
          tab == 1 ?  'color-title' : 'text-white',
          tab == 1 ? '' : 'background-none']" @click="handleClickTab(1)">注册</view>
        </view>
      </view>
      <!-- 登录 -->
      <view class="form" v-if="tab == 0">
        <view class="cu-form-group margin-top background-none">
          <text class='cuIcon-people color-theme margin-right-sm'></text>
          <input placeholder-class="color-title" placeholder="手机号" name="input"></input>
        </view>
        <view :style="{'border-bottom': '1px solid ' + themeColor.title}" class="cu-form-group background-none border-color-title">
          <text class='cuIcon-lock color-theme margin-right-sm'></text>
          <input placeholder-class="color-title" type="password" placeholder="密码6到16位" name="input"></input>
        </view>

        <view class="form-submit text-center">
          <button @click="handleClickLogin" style="width: 80%" class="cu-btn lg bg-theme margin-bottom-lg color-title">
            登录
          </button>
        </view>
      </view>

      <!-- 注册 -->

      <view class="form" v-if="tab == 1">
        <view class="cu-form-group margin-top background-none">
          <text class='cuIcon-people color-theme margin-right-sm'></text>
          <input placeholder-class="color-title" placeholder="手机号" name="input"></input>
        </view>
        <view class="cu-form-group background-none border-color-title">
          <text class='cuIcon-mark color-theme margin-right-sm'></text>
          <input placeholder-class="color-title" placeholder="短信验证码" name="input"></input>
          <button class='cu-btn bg-green shadow bg-theme color-title'>验证码</button>
        </view>



        <view  class="cu-form-group background-none border-color-title">
          <text class='cuIcon-lock color-theme margin-right-sm'></text>
          <input placeholder-class="color-title" type="password" placeholder="密码6到16位" name="input"></input>
        </view>
        <view :style="{'border-bottom': '1px solid ' + themeColor.title}" class="cu-form-group background-none border-color-title">
          <text class='cuIcon-lock color-theme margin-right-sm'></text>
          <input placeholder-class="color-title" type="password" placeholder="确认密码6到16位" name="input"></input>
        </view>

        <view class="form-submit text-center">
          <button @click="handleClickReg" style="width: 80%" class="cu-btn lg bg-theme margin-bottom-lg color-title">
            注册
          </button>
        </view>
      </view>


      <view class="">
        <divider text="其他登录方式" margin-top="120rpx"></divider>
      </view>

      <view class="flex justify-around">
        <view class="cu-avatar round" style="width: 100rpx; height: 100rpx">
          <image  style="width: 80%; height: 80%" src="/static/login/qq.png"></image>
        </view>
        <view class="cu-avatar round" style="width: 100rpx; height: 100rpx">
          <image  style="width: 70%; height: 70%" src="/static/login/weixin.png"></image>
        </view>
      </view>
    </view>
    

  </view>
</template>

<script>
import divider from '@/components/divider'
export default {
  components: {
    divider
  },
  data() {
    return {
      tab: 0
    }
  },
  methods: {
    handleClickTab(i) {
      this.tab = i
    },
    // 登录
    handleClickLogin(e) {
      
    },
    // 注册
    handleClickReg(e) {
      
    },
  },
}
</script>

<style lang="scss" scoped>
.background-none {
  background: none  !important;
}
.solids-bottom {
  border-color: $main-title-color  !important;
}
.border-color-title {
  border-color: $main-title-color;
}
.login {
  .bg-login-box {
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    z-index: -1;
    .bg-login-img {
      width: 100%;
      height: 100%;
      display: block;
    }
  }

  .login-body {
    padding: 200rpx 60rpx 0 60rpx;
    .tab {
      margin-top: 80rpx;
      .tab-box {
        margin: 0 auto;
        width: 340rpx;
        
      }
    }

    
  }

}
</style>