<template lang="pug">
    transition(name="drop")
        div(
            class="dropDownMenu"
            @mouseover="menuAppearance"
            @mouseleave="menuHide"
        )
            ul(class="list")
                li(
                    class="element"
                    v-for="(elem, index) in elements"
                    :key="index"
                )
                    a(:href="`#${elem.anchor}`" class="link") {{elem.name}}

</template>

<script>
    export default {
        name: "DropDownMenu",
        props: {
            elements: Array,
            menuHide: Function,
            menuAppearance: Function,
        },
    }
</script>

<style lang="sass" scoped>
    .drop-enter, .drop-leave-to
        opacity: 0

    .drop-enter-active, .drop-leave-active
        transition: all .5s

    .dropDownMenu
        display: flex
        flex-direction: column
        position: absolute
        background: #2a2a2a
        width: 16%
        height: auto
        z-index: 100

        .list
            display: flex
            flex-direction: column
            height: auto
            width: 100%
            box-sizing: border-box

            .element
                width: 100%
                list-style-type: none
                height: 50px
                border-bottom: 1px solid white

                .link
                    display: flex
                    justify-content: center
                    color: white
                    align-items: center
                    width: 100%
                    height: 100%
                    text-decoration: none

            .element:hover
                background: #424242
</style>