<template lang="pug">
    header
        Logo(v-bind="logo")
        Menu(v-bind="menu")
        Info(v-bind="info")
</template>

<script>
    import Logo from './Logo.vue';
    import Menu from "./Menu.vue";
    import Info from "./Info.vue";

    export default {
        name: "Header",
        props: {
            logo: Object,
            menu: Object,
            info: Object
        },
        components: {Info, Menu, Logo}
    }
</script>

<style lang="sass" scoped>
    header
        background-color: #424242
        width: 100%
        height: 80px
        position: relative
        display: flex
        flex-direction: row
        padding: 0 5% 0 5%
        box-sizing: border-box
</style>