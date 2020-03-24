<template>
  <div class="home">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>

import Header from "@/components/Header.vue";
import Main from "@/components/Main.vue";
import Footer from "@/components/Footer.vue";

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
    display: flex;
    flex-direction: column;
    justify-content: space-between;
  }
</style>
