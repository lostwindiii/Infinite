<template>
  <header class="head-bg" id="head-bg">
    <div class="head">
      <div class="head-left">
        <a href="javascript:;" class="logo"></a>
        <ul class="nav-menu">
          <li class="nav-li nav-on"><a href="javascript:;">主页</a></li>
          <li class="nav-li"><a href="javascript:;">好物</a></li>
          <li class="nav-li"><a href="javascript:;">好店</a></li>
          <li class="nav-li"><a href="javascript:;">关于</a></li>
        </ul>
      </div>
      <div class="head-right">
        <div class="search">
          <i class="search-icon"></i>
          <input class="search-input" type="text" :placeholder='placeholder' @focus='searchFocus' @blur='searchBlur' v-model='searchText'>
        </div>
        <div class="head-login">
          <span class="login"><a href="javascript:;">登录</a></span>
          <span class="register"><a href="javascript:;">注册</a></span>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'head',
  data () {
    return {
      searchText: '',
      placeholder: '搜索'
    }
  },
  mounted () {

  },
  computed: {

  },
  methods: {
    searchFocus () {
      this.isActive = true
      this.placeholder = ''
    },
    searchBlur () {
      this.isActive = false
      this.placeholder = '搜索'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang='scss' scoped>
@import "../style/head.scss"
</style>
