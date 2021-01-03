<template>
  <div id="home">
    <nav-bar class="home-nav">
      <div slot="center">购物街</div>
    </nav-bar>
    <home-swiper :banners="banners"></home-swiper>
    <home-recommend :recommends="recommends"></home-recommend>
    <home-feature></home-feature>
  </div>
</template>

<script>
import NavBar from "components/common/navbar/NavBar";
import { getHomeMultidata } from "network/home";
import { getHomeGoods } from "network/home";
import HomeSwiper from "./childcomps/HomeSwiper";
import HomeRecommend from "./childcomps/HomeRecommend";
import HomeFeature from "./childcomps/HomeFeature";
export default {
  data() {
    return {
      banners:[],
      recommends:[]
    }
  },
  components: {
    NavBar,
    HomeSwiper,
    HomeRecommend,
    HomeFeature,
    getHomeMultidata,
    getHomeGoods,
  },
  created() {
    getHomeMultidata().then((res) => {
      this.banners = res.data.banner.list;
    });
    getHomeMultidata().then((res) => {
      this.recommends = res.data.recommend.list;
    });
  },
};
</script>

<style>
#home {
  padding-top: 44px;
}
.home-nav {
  background-color: var(--color-tint);
  color: white;
  position: fixed;
  top: 0;
  left: 0;
  right:0px;
  z-index: 5;
}
</style>
