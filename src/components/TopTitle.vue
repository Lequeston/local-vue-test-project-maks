<template lang="pug">
    div(id="title-block")
        div(id="title") {{title}}
        div(id="info") {{info}}
</template>

<script>
    export default {
        name: "TopTitle",
        props: {
            title: String,
            info: String
        }
    }
</script>

<style lang="sass" scoped>
    #title-block
        display: flex
        flex-direction: column
        width: 1170px
        padding-top: 100px
        margin: 0 auto
        height: 100%
        color: white

        #title
            font-family: Montserrat, sans-serif,sans-serif
            font-weight: bold
            font-size: 54px

        #info
            font-size: 20px
            margin-top: 20px
</style>