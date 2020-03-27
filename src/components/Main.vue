<template lang="pug">
    div(id="body")
        MainTopPicture(v-bind="mainTopPicture")
        Courses(v-bind="courses")
        Video(v-bind="video")
        GraduateInformation(v-bind="graduateInformation")
        Registration(v-bind="registration")
        GeneralInformation(v-bind="generalInformation")
</template>

<script>
    import Registration from "@/components/Registration.vue";
    import GeneralInformation from "@/components/GeneralInformation.vue";
    import MainTopPicture from "@/components/MainTopPicture";
    import Courses from "@/components/Courses";
    import Video from "@/components/Video";
    import GraduateInformation from "@/components/GraduateInformation";
    export default {
        name: "Main",
        props: {
            courses: Object,
            mainTopPicture: Object,
            video: Object,
            graduateInformation: Object,
            registration: Object,
            generalInformation: Object
        },
        components: {GraduateInformation, Video, Courses, MainTopPicture, GeneralInformation, Registration},
    }
</script>

<style lang="sass" scoped>
    #body
        padding: 0 0 5% 0
        display: flex
        flex-direction: column
        width: 100%
</style>