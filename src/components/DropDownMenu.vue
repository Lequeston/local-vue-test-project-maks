<template lang="pug">
    div(class="dropDownMenu")
        ul(class="list")
            li(
                class="element"
                v-for="(elem, index) in elements"
                :key="index"
            ) {{elem.name}}

</template>

<script>
    export default {
        name: "DropDownMenu",
        props: {
            elements: Array
        }
    }
</script>

<style lang="sass" scoped>
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
            padding: 3px 5px 3px 5px

            .element
                display: flex
                justify-content: center
                align-items: center
                width: 100%
                color: white
                list-style-type: none
                height: 50px
                border-bottom: 1px solid white
</style>