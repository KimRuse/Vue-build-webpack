<template>
    <div class="footer">
      <div class="opts">
        <a href="#" class="opts-group">
          <i></i>
          <span>5</span>
        </a>
        <a href="#" class="opts-group">
          <i></i>
          <span>5</span>
        </a>
        <a href="#" class="opts-group">
          <i></i>
          <span>5</span>
        </a>
        <a href="#" class="opts-group">
          <i></i>
          <span>5</span>
        </a>
        <a href="#" class="opts-group">
          <i></i>
          <span>5</span>
        </a>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style lang="scss" scoped>
  @media screen and (min-width: 991px) {
    .footer {
      display: none;
    }
  }
  .footer {
    position: fixed;
    bottom: 0; left: 0;
    background-color: #fafafa;
    box-shadow: 0 -1px rgba(0,0,0,0.1), 0 -2px 10px rgba(0,0,0,0.1);
    height: 49px; width: 100%;
    line-height: 49px;
    .opts {
      display: flex;
      justify-content: space-around;
      .opts-group {
        float: left;
        line-height: 49px;
      }
    }
  }
</style>