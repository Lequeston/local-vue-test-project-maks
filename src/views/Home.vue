<template lang="pug">
  div(class="home")
    Header(v-bind="information.header")
    Main(v-bind="information.main")
    Footer(v-bind="information.footer")
</template>

<script>

import Header from "@/components/Header.vue";
import Main from "@/components/Main.vue";
import Footer from "@/components/Footer.vue";
import Information from '../assets/information';

export default {
  name: 'Home',
  components: {
    Footer,
    Main,
    Header,
  },
  computed: {
      information(){
          return Information;
      }
  }
}
</script>

<style lang="sass" scoped>
  .home
    display: flex
    flex-direction: column
    justify-content: space-between
</style>
