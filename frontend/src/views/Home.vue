<template>
  <el-row>
    <Navbar style="z-index: 99"></Navbar>
    <Carousel />
    <el-row class="max-width-container">
      <Presentation/>
      <Products />
      <ArqDecor />
      <Partners />
      <Contact />
    </el-row>
    <Footer />
  </el-row>
  
</template>

<style lang="scss">
@import '../styles/variables.scss';
</style>

<script>
import Navbar from "../components/Navbar"
import Carousel from "../components/Home/Carousel"
import Presentation from "../components/Home/Presentation"
import Products from "../components/Home/Products"
import Partners from "../components/Home/Partners"
import Contact from "../components/Home/Contact"
import ArqDecor from "../components/Home/ArqDecor"
import Footer from "../components/Footer"

export default {
  name: 'Home',
  components: {
    Navbar,
    Carousel,
    Presentation,
    Products,
    ArqDecor,
    Partners,
    Contact,
    Footer,
  }
}
</script>
