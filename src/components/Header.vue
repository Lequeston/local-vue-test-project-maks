<template>
    <header>
        <Logo />
        <Menu />
        <Info />
    </header>
</template>

<script>
    import Logo from './Logo.vue';
    import Menu from "@/components/Menu";
    import Info from "@/components/Info";

    export default {
        name: "Header",
        components: {Info, Menu, Logo}
    }
</script>

<style scoped>
    header {
        background-color: black;
        width: 100%;
        height: 100px;
        position: relative;
        display: flex;
        flex-direction: row;
        padding: 1% 5% 1% 5%;
        box-sizing: border-box;
    }
</style>