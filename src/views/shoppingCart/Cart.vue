<template>
  <div>
    <Navbar class="nav-bar">
      <div slot="center">购物</div>
    </Navbar>
  </div>
</template>

<script>
import Navbar from '../../components/common/nav-bar/Navbar'
  export default {
    name: "Cart",
    components:{
      Navbar
    }
  }
</script>

<style scoped>
.nav-bar{
    background: hotpink;
    color:#fff;
    font-size: 18px;
    font-weight:bold ;
  }
</style>
