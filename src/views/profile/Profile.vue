<template>
  <div>
    <Navbar class="nav-bar">
      <div slot="center">我的</div>
    </Navbar>
  </div>
</template>

<script>
import Navbar from '../../components/common/nav-bar/Navbar'
  export default {
    name: "Profile",
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
