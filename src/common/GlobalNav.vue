<template>
  <div class="global-nav">
    <div class="contain">
      <Header />
      <Footer />
    </div>
  </div> 
</template>

<script>
import Header from './components/Header.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'GlobalNav',
  components: {
    Header, Footer
  }
}
</script>

<style lang="scss">
  @media screen and (min-width: 320px) {
    .contain {
      min-width: 320px;
      .show {
        display: none;
      }
      .header {
        height: 44px;
        line-height: 44px;
        display: flex;
        justify-content: space-between;
        .h-search, .h-login{
          font-weight: bold; 
          text-align: center;
          line-height: 44px;
          i {
            font-size: 24px;
            margin: 0 15px;
          }
        }
        .h-title img {
          height: 32px;
          background-size: auto 32px; 
          transform: translateY(6.5px);
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
            color: #ccc;
            transform: translateY(-8px);
            &.active {
              color: #009a61;
            }
            span {
              font-size: 12px;
              display: block;
              margin: -30px -3px;
            }
          }
        } 
      }
    }
  }
  @media screen and (min-width: 760px) {
    .contain {
      width: 750px;
      margin: 0 auto;
    }
  }
  @media screen and (min-width: 1062px) {
    .footer {
      display: none;
    }
    .contain {
      width: 90%;
      .show {
        display: block;
      }
      .show-i {
        display: none;
      }
      .header {
        display: block;
        color: #ccc;
        height: 64px;
        line-height: 64px;
        .h-title {
          position: absolute;
          left: 30px;
          img {
            transform: translateY(10px);
          }
        }
        .h-search {
          position: absolute;
          left: 320px;
          order: 1;
          input {
            width: 200px;
            height: 45px;
            border-radius: 4px;
            margin: 10px;
            transition: all .5s ease-out;
            &::-webkit-input-placeholder {
              opacity:0.5;
            }
          }
        }
        .h-nav {
          position: absolute;
          left: 230px;
          a {
            display: inline-block;
            line-height: 40px;
            border-radius: 6px;
            padding: 0 7px;
            color: #ccc;
            margin: 0 7px;
            &.active {
              color: #009a61;
            }
            &:hover {
              background: #f3f3f3;
            }
          }
        }
      }
    }
    .h-login {
      position: absolute;
      right: 30px;
      top: 13px;
      color: #009a61;
      .show-i {
        display: block;
      }
      .show {
        display: none;
      }
    }
  }
  @media screen and (min-width: 1180px) {
    
    .h-login {
      .show {
        display: block;
      }
      .show-i {
        display: none;
      }
      position: absolute;
      right: 30px;
      top: 0;
      span {
        cursor: pointer;
        display: inline-block;
        height: 40px;
        line-height: 40px;
        padding: 0 7px;
        margin: 12px 0;
        border-radius: 6px;
        &:nth-of-type(1) {
          color: #009a61;
          margin-right: 15px;
          &:hover {
            background: #f3f3f3;
          }
        }
        &:nth-of-type(2) {
          background-color: #009a61;
          color: #fafafa;
        }
      }
    }
  }
  .global-nav {
    border-top: 3px solid #009a61;
    box-shadow: 0px 2px 10px 0px rgba(0,0,0,0.1), 0 1px rgba(0,0,0,0.1);
    background: #fafafa;
  }
</style>
