<template>
  <div>
    <box class="mainWidth textCenter">
      <x-img :src="showUrl" class="show"></x-img>
      <box class="welcome-font">欢迎来访!</box>
      <box class="enter-page">
        <router-link to="HelloWorld">进入页面 >></router-link>
      </box>
    </box>
  </div>
</template>

<script>
  import {Group, Cell, Box, XImg} from 'vux'
  import showUrl from '../assets/images/show.png'

  export default {
    components: {
      XImg,
      Box,
      Group,
      Cell
    },
    data () {
      return {
        showUrl: showUrl,
        msg: 'Hello World!',
      }
    }
  }
</script>

<style>
  .show {
    width: 240px;
    margin-top: 80px;
  }

  .welcome-font {
    margin-top: 30px;
    color: #ffffff;
    font-size: 18px;
    letter-spacing: 2px;
  }

  .enter-page {
    margin-top: 100px;
    text-decoration: underline;
  }

  .enter-page a {
    color: #fff;
  }
</style>
