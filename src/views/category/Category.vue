<template>
  <div>
    <Navbar class="nav-bar">
      <div slot="center">分类</div>
    </Navbar>
  </div>
</template>

<script>
import Navbar from '../../components/common/nav-bar/Navbar'
  export default {
    name: "Category",
    components:{
      Navbar
    }
  }
</script>

<style scoped>
.nav-bar{
    background: palevioletred;
    color:#fff;
    font-size: 18px;
    font-weight:bold ;
  }
</style>
