<template>
  <swiper>
    <swiper-item v-for="item in banners" :key="item.title">
      <a :href="item.link">
        <img :src="item.image" :alt="item.title">
      </a>
    </swiper-item>
  </swiper>
</template>

<script>
import { Swiper, SwiperItem } from "components/common/swiper";
import {getHomeMultidata} from "network/home";
import {getHomeGoods} from "network/home";
export default {
  data() {
    return {
      banners: [],
    };
  },
  created() {
    getHomeMultidata().then((res) => {
      this.banners = res.data.banner.list;
    });
  },
  components:{
    Swiper,
    SwiperItem
  }
};
</script>

<style>
</style>
