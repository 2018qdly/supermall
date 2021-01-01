<template>
  <div id="app">
    <tab-bar>
      <tab-bar-item>
        <div slot="item-text">首页</div>
      </tab-bar-item>
      <tab-bar-item>
        <div slot="item-text">分类</div>
      </tab-bar-item>
      <tab-bar-item>
        <div slot="item-text">购物车</div>
      </tab-bar-item>
      <tab-bar-item>
        <div slot="item-text">我的</div>
      </tab-bar-item>
    </tab-bar>
  </div>
</template>

<script>
import TabBar from './components/common/TabBar/TabBar'
import TabBarItem from './components/common/TabBar/TabBarItem'

export default {
  name: 'App',
  components: {
    TabBar,
    TabBarItem
  }
}
</script>

<style>
  @import 'assets/css/base.css';
</style>


