<template>
    <div class="header">
      <div class="h-search">S</div>
      <div class="h-title">title</div>
      <div class="h-login">L</div>
    </div>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style lang="scss" scoped>
  .header {
    height: 64px;
    line-height: 64px;
    display: flex;
    justify-content: space-between;
    .h-search {
      padding: 15px;
      text-align: center;
      line-height: 32px;
    }
    .h-login {
      padding: 15px;
      text-align: center;
      line-height: 32px;
    }
  }
</style>

