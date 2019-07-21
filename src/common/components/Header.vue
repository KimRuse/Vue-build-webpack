<template>
    <div class="header">
      <div class="h-search">
        <i class="iconfont show-i">&#xe61c;</i>
        <input type="text" placeholder="搜索问起或关键字" class="h-search show" :style=" focusState ? activeClass : '' " @focus="handleInput"
         @blur="handleInputOut">
        <div class="h-search-info">

        </div>
      </div>
      <div class="h-nav show">
        <a href="#" class="active">首页</a>
        <a href="#" class="">问答</a>
        <a href="#" class="">专栏</a>
        <a href="#" class="">课程</a>
        <a href="#" class="">圈子</a>
        <a href="#" class="">发现</a>
      </div>
      <div class="h-title">
        <img src="../../../public/logo-b.svg" alt="" class="">
      </div>
      <div class="h-login">
        <i class="iconfont show-i">&#xe639;</i>
        <div class="h-login-l show">
          <span>立即登录</span>
          <span>免费注册</span>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      activeClass: {
       width: '300px'
      },
      focusState: false
    }
  },
  methods: {
    handleInput() {
      this.focusState = true
    },
    handleInputOut() {
      this.focusState = false
    }
  },
}
</script>

<style lang="scss" scoped>
</style>

