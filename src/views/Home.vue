<template>
  <div class="home">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>

import Header from "@/components/Header";
import Main from "@/components/Main";
import Footer from "@/components/Footer";

export default {
  name: 'Home',
  components: {
    Footer,
    Main,
    Header
  }
}
</script>

<style scoped>
  .home{
    height: 2000px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
</style>
