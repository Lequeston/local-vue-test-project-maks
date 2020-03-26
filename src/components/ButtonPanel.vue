<template lang="pug">
    div(class="button-panel")
        a(href="#ourCourses" class="link")
            button(class="button button-left" v-on:click="onClickLeftButton")
        a(href="#ourCourses" class="link")
            button(class="button button-right" v-on:click="onClickRightButton")
</template>

<script>
    export default {
        name: "ButtonPanel",
        props: {
            onClickRightButton: Function,
            onClickLeftButton: Function,
        }
    }
</script>

<style lang="sass" scoped>
    .button-panel
        margin-top: 10px
        display: flex
        flex-direction: row
        align-items: center
        justify-content: center
        align-content: center
        width: 100%
        height: auto
        box-sizing: border-box
        padding: 0 15% 0 15%

        $width: 40px
        .link
            width: $width
            height: $width
            text-decoration: none

            .button
                display: flex
                justify-content: center
                align-items: center
                background: inherit
                border: 1px solid #424242
                border-radius: 50%
                font-size: $width
                color: #424242
                width: 100%
                height: 100%

            .button-right
                margin-left: 20px

            .button-left:after
                content: '\003C'


            .button-right:after
                content: '\003E'
</style>