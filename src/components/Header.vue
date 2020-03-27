<template lang="pug">
    div
        header
            Logo(v-bind="logo")
            Menu(
                v-bind="menu"
                :menuAppearance="menuAppearance"
                :menuHide="menuHide"
            )
            Info(v-bind="info")
        dropDownMenu(
            v-show="isVisible"
            class="dropMenu"
            v-bind="dropMenuRight"
            :menuAppearance="menuAppearance"
            :menuHide="menuHide"
        )
</template>

<script>
    import Logo from './Logo.vue';
    import Menu from "./Menu.vue";
    import Info from "./Info.vue";
    import DropDownMenu from "./DropDownMenu.vue";

    export default {
        name: "Header",
        props: {
            logo: Object,
            menu: Object,
            info: Object,
            dropMenuRight: Object
        },
        data(){
            return{
                isVisible: false,
            }
        },
        methods: {
           menuAppearance(){
               this.isVisible = true;
           },
           menuHide(){
               this.isVisible = false;
           }
        },
        components: {Info, Menu, Logo, DropDownMenu}
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

    .dropMenu
        margin-left: 57%
</style>