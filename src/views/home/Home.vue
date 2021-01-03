<template>
  <div id="home">
    <nav-bar class="home-nav"><div slot="center">购物街</div></nav-bar>
    <home-swiper></home-swiper>
  </div>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'
import HomeSwiper from './childcomps/HomeSwiper'
export default {
  components: {
    NavBar,
    HomeSwiper
  },


};
</script>

<style>
  .home-nav {
    background-color: var(--color-tint);
    color: white;
  }
</style>
