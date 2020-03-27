<template lang="pug">
    div(id="main-top-picture")
        div(id="main-top-background")
            TopTitle(v-bind="topTitle")
        a(class="button" :href="`#${buttonLink}`") {{buttonName}}
</template>

<script>
    import TopTitle from "@/components/TopTitle";
    export default {
        name: "MainTopPicture",
        props: {
            buttonName: String,
            buttonLink: String,
            info: String,
            topTitle: Object
        },
        components: {TopTitle}
    }
</script>

<style lang="sass" scoped>
    #main-top-picture
        display: flex
        background-image: url("../assets/background-town.jpg")
        width: 100%
        height: 650px
        background-position: center

        #main-top-background
            padding-top: 50px
            background: black
            width: 100%
            height: 600px
            opacity: 0.5
            position: absolute
            z-index: 1

        .button
            display: flex
            width: 350px
            height: 60px
            background: rgb(245, 85, 14)
            border: none
            opacity: 0.8
            border-radius: 100px
            position: relative
            z-index: 3
            margin: auto auto 20% auto
            color: white
            font-size: 25px
            font-weight: 200
            justify-content: center
            align-self: center
            align-items: center
            text-decoration: none

        .button:hover
            opacity: 1

</style>