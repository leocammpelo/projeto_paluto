<template>
  <el-row>
    <Navbar style="z-index: 99"></Navbar>
    <Carousel />
  </el-row>
  
</template>

<style lang="scss">
@import '../styles/variables.scss';
</style>

<script>
import Navbar from "../components/Navbar"
import Carousel from "../components/Home/Carousel"

export default {
  name: 'Home',
  components: {
    Navbar,
    Carousel,
  }
}
</script>
