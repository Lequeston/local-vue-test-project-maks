<template lang="pug">
    footer
        Logo
</template>

<script>
    import Logo from "./Logo.vue";

    export default {
        name: "Footer",
        components: {Logo}
    }
</script>

<style lang="sass" scoped>
    footer
        background-color: slategray
        width: 100%
        height: 80px
        position: relative
        display: flex
        flex-direction: row
        padding: 1% 5% 1% 5%
        box-sizing: border-box
</style>