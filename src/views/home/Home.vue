<template>
  <div>
    <div id="home">
      <nav-bar class="home-nav"><div slot="center">购物街</div></nav-bar>
      <home-swiper :banners="banners"></home-swiper>
      <recommend-view :recommends="recommends" class="recommend"></recommend-view>
      <feature-view></feature-view>
      <tab-control :titles="titles" class="tab-control"></tab-control>
      <ul>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        <li>a</li>
        </ul>
    </div>
  </div>
</template>

<script>
// 子组件
import HomeSwiper from './childComps/HomeSwiper'
import RecommendView from './childComps/RecommendView'
import FeatureView from './childComps/FeatureView'
// 公共组件
import NavBar from 'components/common/navbar/NavBar'
import TabControl from 'components/content/tabControl/TabContorl'
// network
import {getHomeMultidata} from 'network/home'



export default {
  name: "Home",
  data() {
    return {
      banners: [],
      recommends: [],
      titles:['流行','新款','精选'],
    };
  },
  components: {
    NavBar,
    HomeSwiper,
    RecommendView,
    FeatureView,
    TabControl
  },
  created() {
    getHomeMultidata().then(res => {
      console.log(res);
      this.banners= res.data.banner.list;
      this.recommends= res.data.recommend.list;
    })
  }
};
</script>

<style  scoped>
  .home-nav {
    background-color: var(--color-tint);
    color: var(--color-background);
    position: fixed;
    left: 0;
    right: 0;
    top: 0;
    z-index: 9;
  }
  #home {
    padding-top: 44px;
  }
  /* .recommend {
    margin-bottom: 10px;
  } */
  .tab-control {
    /* 吸顶效果 */
    position: sticky;
    top: 44px;
  }
</style>