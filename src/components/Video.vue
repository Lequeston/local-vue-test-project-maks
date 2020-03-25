<template lang="pug">
    div(class="video")
        iframe(class="content" src="https://www.youtube.com/embed/t8zwdpkSRWs" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen)
</template>

<script>
    export default {
        name: "Video"
    }
</script>

<style lang="sass" scoped>

    .video
        width: 940px
        height: 530px
        position: relative
        margin: 30px auto 0 auto

        .content
            width: 100%
            height: 100%

</style>