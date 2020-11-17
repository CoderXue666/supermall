<template>
  <div id="home">
    <NavBar class="home-nav"><div slot="center">购物街</div></NavBar>
    <HomeSwiper :banner="banner"></HomeSwiper>
    <HomeRecommends :recommend="recommend"/>
    <feature-view />
    <TabControl :title="['流行','新款','精选']" class="tab-control-top"/>
    <ul>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
      <li>列表</li>
    </ul>
  </div>
</template>

<script>
import HomeSwiper from "./chidComs/HomeSwiper";
import HomeRecommends from "./chidComs/HomeRecommends";
import FeatureView from "./chidComs/FeatureView";

import NavBar from "components/common/navbar/NavBar";
import TabControl from "components/content/tabControl/TabControl";

import {getHomeMultidata} from "network/home";
//import Swiper from "components/common/swiper/Swiper";
//import SwiperItem from "components/common/swiper/Swiperitem";

export default {
  name: "Home",
  components: {
    HomeSwiper,
    HomeRecommends,
    FeatureView,

    NavBar,
    TabControl
  },
  data() {
    return {
      //result: null,
      banner: [],
      recommend: []
    }
  },
  created() {
    //1.请求多个数据
    getHomeMultidata().then(res => {
      //this.result = res;
      this.banner = res.data.banner.list;
      this.recommend = res.data.recommend.list;
    })
  }
}
</script>

<style scoped>
 #home{
   padding-top: 44px;
 }
 .home-nav {
   background-color: var(--color-tint);
   color: #fff;

   position: fixed;
   left: 0;
   right: 0;
   top: 0;
   z-index: 9;
 }

 .tab-control-top {
   position: sticky;
   top: 44px;
 }
</style>
