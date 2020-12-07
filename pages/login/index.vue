<template>
  <view class="login">
    <view class="bg-login-box">
      <image mode="" class="bg-login-img" src="/static/login/bg-login.jpg"></image>
    </view>

    <!-- TODO: 登录 注册表单   -->


    <view class="login-btns text-center width-max">
      <button @click="handleClickBtn($event, 'login')" class="cu-btn lg bg-theme margin-bottom-lg color-title">
        登录<text class="icon cuIcon-right color-title"></text>
      </button>
      <button @click="handleClickBtn($event, 'reg')" class="cu-btn lg bg-icon color-title">
        注册<text class="icon cuIcon-right color-title"></text>
      </button>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      
    }
  },
  methods: {
    handleClickBtn(e, type) {

    }    
  },
}
</script>

<style lang="scss" scoped>
.login {
  .bg-login-box {
    position: fixed;
    width: 100vw;
    height: 100vh;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
    z-index: 0;
    .bg-login-img {
      width: 100%;
      height: 100%;
      display: block;
    }
  }

  .login-btns {
    position: absolute;
    bottom: 200rpx;
    left: 0;
    
    .cu-btn {
      width: 70%;
      opacity: 0.7;
      .icon {
        position: absolute;
        right: 30rpx;
        top: 50%;
        transform: translateY(-50%);
      }
    }

    
  }
}
</style>