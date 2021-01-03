<template>
  <div class="tab-control">
    <div
    v-for="(item,index) in titles"
    class="tab-control-item"
    :class="{active:curindex === index}"
    @click="itemclick(index)"
    >
      <span>{{item}}</span>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      curindex:0
    }
  },
  props: {
    titles: {
      type: Array,
      default() {
        return [];
      },
    },
  },
  methods:{
    itemclick(index) {
      this.curindex = index
    }
  }
};
</script>

<style>
.tab-control {
  display: flex;
  text-align: center;
  font-size: 15px;
  height: 40px;
  line-height: 40px;
}
.tab-control-item {
  flex: 1;
}
.active {
  color:deeppink;
}
.active span {
  border-bottom:deeppink 2px solid;
  padding: 3px;
}
</style>
