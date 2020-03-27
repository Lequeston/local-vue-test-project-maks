<template lang="pug">
    div(id="block-text")
        h5(id="information_title" class="title") {{title}}
        p(id="text") {{text}}
</template>

<script>
    export default {
        name: "GeneralInformation",
        props: {
            title: String,
            text: String
        }
    }
</script>

<style lang="sass" scoped>
    #block-text
        margin-top: 3%
        width: 90%
        padding: 3% 5% 3% 5%
        height: auto
        color: black

        .title
            font-size: 20px

        #text
            margin-top: 1%
            white-space: pre-wrap
</style>