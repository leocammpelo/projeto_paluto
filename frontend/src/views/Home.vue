<template>
  <el-row>
    <Navbar style="z-index: 99"></Navbar>
    <Carousel />
    <el-row class="max-width-container">
      <Presentation/>
    </el-row>
  </el-row>
  
</template>

<style lang="scss">
@import '../styles/variables.scss';
</style>

<script>
import Navbar from "../components/Navbar"
import Carousel from "../components/Home/Carousel"
import Presentation from "../components/Home/Presentation"

export default {
  name: 'Home',
  components: {
    Navbar,
    Carousel,
    Presentation,
  }
}
</script>
