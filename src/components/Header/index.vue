<template>
  <div class="header-box">
    <div class="header">
        <div class="float-left logo">
          <router-link to="/">
            <img src="../../assets/common/logo.png" alt="">
            <span class="name">中文社区</span>
          </router-link>
        </div>
        <div class="right-box">
          <div class="search-box">
            <input type="text" class="search">
          </div>
          <button type="button" class="btn btn-primary btn-sm">
            <router-link to="/add">+ 发帖</router-link>
          </button>
          <div class="notice">
            <router-link to="/notification"><i class="iconfont">&#xe634;</i><span class="badge badge-danger">5</span></router-link>
          </div>
          <div class="avatar">
              <router-link to="/homepage">
                <img src="../../assets/logo.png" alt="">
              </router-link>
              <div class="dropdown">
                <div><router-link to="/profile/basic"><i class="iconfont">&#xe679;</i> 我的主页</router-link></div>
                <div><router-link to="/profile/basic"><i class="iconfont">&#xe675;</i> 设置</router-link></div>
                <div><a href=""><i class="iconfont">&#xe6e3;</i> 退出</a></div>
              </div>
          </div>
          <div class="log-box">
            <span><router-link to="/register">注册</router-link></span>
            |
            <span><router-link to="/login">登陆</router-link></span>
          </div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      msg: ''
    }
  },
  methods: {
    handleClick: function () {
      alert(1)
    }
  }
}
</script>

<style lang="scss" scoped>
  .name {
      font-weight: bolder;
  }
  .header-box {
      width: 100%;
      height: 45px;
      background: #fff;
      position: absolute;
      left: 0;
      top: 0;
      .header {
          display: flex;
          width: 1120px;
          height: 100%;
          align-items: center;
          justify-content: space-between;
          line-height: 45px;
          margin: 0 auto;
      }
  }
  .right-box {
    height: 45px;
    line-height: 45px;
  }
  .right-box > div {
    display: inline-block;
  }
  .avatar {
    width: 40px;
    height: 100%;
    cursor: pointer;
    position: relative;
    img {
      width: 100%;
      vertical-align: middle;
    }
  }
  .dropdown {
    display: none;
    position: absolute;
    left: -30px;
    top: 50px;
    width: 110px;
    padding: 5px 0;
    background: #fff;
    box-shadow: 0 5px 20px rgba(26,26,26,.1);
    border-radius: 2px;
    &>div {
      height: 30px;
      line-height: 30px;
      padding: 0px 10px;
      transition: all 0.3s ease;
      &:hover {
        background: #ccc;
      }
    }
  }
  .search {
    width: 300px;
    height: 30px;
    background: inherit;
    background-color: rgba(242, 242, 242, 1);
    box-sizing: border-box;
    border-width: 1px;
    border-style: solid;
    border-color: rgba(204, 204, 204, 1);
    border-radius: 5px;
    -moz-box-shadow: none;
    -webkit-box-shadow: none;
    box-shadow: none;
  }
  .log-box {
    display: inline-block;
    width: 100px;
    height: 30px;
    line-height: 30px;
    text-align: center;
    border: 1px solid #ccc;
    border-radius: 5px;
    font-weight: 700;
    font-size: 14px;
    color: #092D1F;
  }
  .logo {
    img {
      vertical-align: -9px;
    }
  }
  a:hover {
    text-decoration: none;
  }
  .notice .badge {
    position: relative;
    top: -10px;
    left: -6px;
  }
  .btn a {
    color: #fff;
  }
</style>
