<template>
  <div class="wrapper-header">
    <Menu mode="horizontal" theme="dark" active-name="1">
      <div class="wrapper-header-nav">
        <router-link to="/" exact-active-class="wrapper-header-nav-logo">
            <img src="../assets/logo.png" alt=""/>
        </router-link>
        <div class="wrapper-header-nav-list">
            <menu-item name="1">
              <Icon type="ios-navigate"></Icon>
              Item 1
            </menu-item>
            <menu-item name="2">
              <Icon type="ios-keypad"></Icon>
              Item 2
            </menu-item>
            <menu-item name="3">
              <Icon type="ios-analytics"></Icon>
              Item 3
            </menu-item>
            <menu-item name="4">
              <Icon type="ios-paper"></Icon>
              Item 4
            </menu-item>
        </div>
      </div>
    </Menu>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data () {
    return {
      isCollapsed: false
    }
  },
  computed: {
  }
}
</script>
<style scoped>
  .wrapper-header{
    position: fixed;
    width: 100%;
    top: 0;
    right: 0;
    z-index: 1000;
  }
  .wrapper-header .ivu-menu-horizontal {
    height: 65px;
    line-height: 65px;
  }
  .wrapper-header .ivu-menu {
    z-index: 901;
    box-shadow: 0 1px 1px rgba(0,0,0,.08);
  }
  .wrapper-header-nav{
    width: 95%;
    height: 65px;
    margin: 0 auto;
  }
  .wrapper-header-nav-logo {
    height: 50px;
    margin-top: 8px;
    float: left;
  }
  .wrapper-header-nav-list {
    height: inherit;
    float: right;
  }
  .wrapper-header-nav-list:after {
    content: "";
    display: block;
    clear: both;
  }
  .wrapper-header-nav-logo img {
    height: 100%;
  }
</style>
