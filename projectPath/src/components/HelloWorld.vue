<template>
  <div>
    <divider> Horizontal </divider>
    <flexbox>
      <flexbox-item><div class="flex-demo vux-1px-l">1</div></flexbox-item>
      <flexbox-item><div class="flex-demo">2</div></flexbox-item>
    </flexbox>
    <divider>woshi nihao</divider>
    <flexbox orient="vertical">
      <flexbox-item>星星</flexbox-item>
      <flexbox-item>月亮</flexbox-item>
      <flexbox-item>太阳</flexbox-item>
    </flexbox>
    <div style="width: 300px; height: 60px; " class="vux-1px-b">sdsdsd</div>
    <span class="vue-close" style="color: red"></span>
    <toast></toast>
    <div>
      <x-switch title="切换出现对话框" v-model="showshow"></x-switch>
    </div>

    <x-dialog v-model="showshow">
      <p>我是一句话</p>
      <div @click="showshow=false">
        <span class="vux-close" style="color: red"></span>
      </div>
    </x-dialog>

  </div>
</template>

<script>
  //引入组件
  import { Group, Divider, Flexbox,  FlexboxItem, Toast, Popup } from 'vux'
  import XSwitch from "../../node_modules/vux/src/components/x-switch/index";

  //创造构造器
  export default {
    components: {
      XSwitch,
      Popup,
      Divider,
      Flexbox,
      FlexboxItem,
      Group,
      Toast
    },
    data () {
      return {
        show: true,
        showshow: false
      }
    }
  }
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  h1, h2 {
    font-weight: normal;
  }

  ul {
    list-style-type: none;
    padding: 0;
  }

  li {
    display: inline-block;
    margin: 0 10px;
  }

  a {
    color: #42b983;
  }
</style>
