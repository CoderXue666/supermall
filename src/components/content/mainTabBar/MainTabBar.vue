<template>
  <TabBar>

    <!--首页-->
    <TabBarItem path="/home">
      <div slot="item-icon"><Icon type="md-home"/></div>
      <div slot="item-icon-active"><Icon type="md-home" color="skyblue"/></div>
      <div slot="item-text">首页</div>
    </TabBarItem>

    <!--分类-->
    <TabBarItem path="/category">
      <div slot="item-icon"><Icon type="ios-apps" /></div>
      <div slot="item-icon-active"><Icon type="ios-apps" color="skyblue"/></div>
      <div slot="item-text">分类</div>
    </TabBarItem>

    <!--购物车-->
    <TabBarItem path="/cart">
      <div slot="item-icon"><Icon type="ios-cart"/></div>
      <div slot="item-icon-active"><Icon type="ios-cart" color="skyblue"/></div>
      <div slot="item-text">购物车</div>
    </TabBarItem>

    <!--我的-->
    <TabBarItem path="/profile">
      <div slot="item-icon"><Icon type="md-contact" /></div>
      <div slot="item-icon-active"><Icon type="md-contact" color="skyblue"/></div>
      <div slot="item-text">我的</div>
    </TabBarItem>

  </TabBar>
</template>

<script>
import TabBar from 'components/common/tabbar/TabBar'
import TabBarItem from "components/common/tabbar/TabBarItem";
export default {
  name: "MainTabBar",
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style scoped>

</style>
