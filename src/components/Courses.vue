<template lang="pug">
    div(id="ourCourses" class="courses")
        div(class="title") {{title}}
        InformationBlock(
            v-for="info in informationBlocks"
            :key="info.id"
            v-bind="getInfo(info)"
        )
</template>

<script>
    import InformationBlock from "@/components/InformationBlock.vue";

    export default {
        name: "Courses",
        props:{
            informationBlocks: Array,
        },
        methods: {
            getInfo(info){
                let newInfo = {...info};
                delete newInfo.id;
                return newInfo;
            }
        },
        data(){
            return{
                title: 'Наши курсы',
            }
        },
        components: {
            InformationBlock,
        }
    }
</script>

<style lang="sass" scoped>
    .courses
        margin-top: 30px
        display: flex
        flex-direction: column
        width: 100%

        .title
            display: flex
            justify-content: center
            font-weight: bold
            font-size: 30px
</style>