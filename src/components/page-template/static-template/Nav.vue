<template>
<div class="NavDiv">
  <ul class="NavUl">
    <li class="NavLi"><router-link class="NavA" to="home">主页</router-link></li>
    <li class="NavLi"><router-link class="NavA" to="find">招聘信息</router-link></li>
    <li class="NavLi" v-if="this.$store.state.jurisdiction.apply==true||this.$store.state.jurisdiction.management==true"><router-link class="NavA" to="apply">求职信息</router-link></li>
    <li class="NavLi"><router-link class="NavA" to="real-name-authentication" v-if="this.$store.state.jurisdiction.realNameAuthentication==true&&this.$store.state.jurisdiction.management==false">实名认证</router-link></li>
  </ul>
</div>
</template>

<script>
export default {
  name: 'Nav',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import "../../../styles/page-template/static-template/Nav.css";
</style>
