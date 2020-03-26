<template lang="pug">
    div(id="ourCourses" class="courses")
        div(class="title") {{title}}
        InformationBlock(
            v-for="info in viewArray"
            :key="info.id"
            v-bind="getInfo(info)"
        )
        ButtonPanel(
            :onClickRightButton="onClickRightButton"
            :onClickLeftButton="onClickLeftButton"
        )
</template>

<script>
    import InformationBlock from "@/components/InformationBlock.vue";
    import ButtonPanel from "@/components/ButtonPanel";

    const DEFAULT_COUNT_VIEW = 4;

    export default {
        name: "Courses",
        props:{
            informationBlocks: Array,
        },
        data(){
            return{
                title: 'Наши курсы',
                visibleRange: {
                    start: 0,
                    end: DEFAULT_COUNT_VIEW,
                }
            }
        },
        computed:{
            viewArray(){
                let {start, end} = this.visibleRange;
                let {informationBlocks} = this;
                return informationBlocks.slice(start, end);
            }
        },
        methods: {
            getInfo(info){
                let newInfo = {...info};
                delete newInfo.id;
                return newInfo;
            },
            onClickRightButton(){
                let {start, end} = this.visibleRange;
                let length = this.informationBlocks.length;
                if (start + DEFAULT_COUNT_VIEW > length){
                    start = 0;
                    end = DEFAULT_COUNT_VIEW;
                } else {
                    start = start + DEFAULT_COUNT_VIEW;
                    end = (end + DEFAULT_COUNT_VIEW > length) ? length : (end + DEFAULT_COUNT_VIEW);
                }
                this.visibleRange.start = start;
                this.visibleRange.end = end;
            },
            onClickLeftButton(){
                let {start, end} = this.visibleRange;
                let length = this.informationBlocks.length;
                if (end - DEFAULT_COUNT_VIEW === 0){
                    start = length - (length % DEFAULT_COUNT_VIEW);
                    end = length;
                } else if ((end - start) < DEFAULT_COUNT_VIEW){
                    end = length - (length % DEFAULT_COUNT_VIEW);
                    start = end - DEFAULT_COUNT_VIEW;
                } else {
                    end -= DEFAULT_COUNT_VIEW;
                    start -= DEFAULT_COUNT_VIEW;
                }
                this.visibleRange.start = start;
                this.visibleRange.end = end;
            }
        },
        components: {
            ButtonPanel,
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