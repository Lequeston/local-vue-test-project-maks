<template>
    <header>
        <Logo />
        <Menu />
        <Info />
    </header>
</template>

<script>
    import Logo from './Header/Logo.vue';
    import Menu from "./Header/Menu.vue";
    import Info from "./Header/Info.vue";

    export default {
        name: "Header",
        components: {Info, Menu, Logo}
    }
</script>

<style scoped>
    header {
        background-color: slategray;
        width: 100%;
        height: 100px;
        position: relative;
        display: flex;
        flex-direction: row;
        padding: 1% 5% 1% 5%;
        box-sizing: border-box;
    }
</style>