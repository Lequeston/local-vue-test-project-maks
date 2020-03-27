<template lang="pug">
    footer
        p(class="text") &copy;{{text}}
</template>

<script>
    export default {
        name: "Footer",
        props:{
            text: String
        },
        components: {}
    }
</script>

<style lang="sass" scoped>
    footer
        background-color: #424242
        width: 100%
        height: 80px
        position: relative
        display: flex
        flex-direction: row
        box-sizing: border-box
        justify-content: space-between
        padding: 10px 30px 10px 30px
        align-items: center
        align-content: center

        .text
            color: white
</style>