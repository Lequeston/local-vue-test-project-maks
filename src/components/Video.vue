<template lang="pug">
    div(class="block-video" id="video")
        div(class="title") {{title}}
        div(class="video")
            iframe(class="content" :src="videoLink" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)
</template>

<script>
    export default {
        name: "Video",
        props: {
            title: String,
            videoLink: String,
        }
    }
</script>

<style lang="sass" scoped>
    .block-video
        width: 100%
        height: auto
        display: flex
        justify-content: center
        align-items: center
        flex-direction: column

        .title
            display: flex
            justify-content: center
            font-weight: bold
            font-size: 30px
            margin-top: 30px

        .video
            width: 940px
            height: 530px
            position: relative
            margin: 30px auto 0 auto

            .content
                width: 100%
                height: 100%

</style>