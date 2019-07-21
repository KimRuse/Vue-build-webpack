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
        <div class="chunk-move" :style="{left: distance + 'px'}"></div>
        <a href="#" class="active" data-num=0 @mouseover="handleNavOver" @mouseout="handleNavOut">首页</a>
        <a href="#" class="" data-num=1 @mouseover="handleNavOver" @mouseout="handleNavOut">问答</a>
        <a href="#" class="" data-num=2 @mouseover="handleNavOver" @mouseout="handleNavOut">专栏</a>
        <a href="#" class="" data-num=3 @mouseover="handleNavOver" @mouseout="handleNavOut">课程</a>
        <a href="#" class="" data-num=4 @mouseover="handleNavOver" @mouseout="handleNavOut">圈子</a>
        <a href="#" class="" data-num=5 @mouseover="handleNavOver" @mouseout="handleNavOut">发现</a>
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
      distance: 0,
      focusState: false
    }
  },
  methods: {
    handleInput() {
      this.focusState = true
    },
    handleInputOut() {
      this.focusState = false
    },
    handleNavOver(event) {
      this.distance = 60 * event.target.dataset['num'];
    },
    handleNavOut() {
      this.distance = 0;
    }
  },
}
</script>

