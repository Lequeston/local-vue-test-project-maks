<template>
    <header>
        <Logo />
        <Menu />
        <Info />
    </header>
</template>

<script>
    import Logo from './Logo.vue';
    import Menu from "./Menu.vue";
    import Info from "./Info.vue";

    export default {
        name: "Header",
        components: {Info, Menu, Logo}
    }
</script>

<style scoped>
    header {
        background-color: slategray;
        width: 100%;
        height: 80px;
        position: fixed;
        display: flex;
        flex-direction: row;
        padding: 1% 5% 1% 5%;
        box-sizing: border-box;
    }
</style>