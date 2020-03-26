<template lang="pug">
    div(class="graduate-information")
        div(class="title") {{title}}
        div(class="information") {{info}}
        Slider(class="slider")
</template>

<script>
    import Slider from "@/components/Slider";
    export default {
        name: "GraduateInformation",
        data(){
            return{
                title: "Наши выпускники",
                info: "Единство предмета речи — это тема высказывания. Тема — это смысловое ядро текста, конденсированное и обобщённое содержание текста.\n" +
                    "\n" +
                    "Понятие «содержание высказывания» связано с категорией информативности речи и присуще только тексту. Оно сообщает читателю индивидуально-авторское понимание отношений между явлениями, их значимости во всех сферах придают ему смысловую цельность. ",
            }
        },
        components: {Slider}
    }
</script>

<style lang="sass" scoped>
    .graduate-information
        display: flex
        flex-direction: row
        flex-wrap: wrap
        width: 94%
        height: auto
        padding: 30px 3% 0 3%

        .title
            display: flex
            justify-content: center
            margin-bottom: 20px
            margin-left: 10px
            width: 100%
            height: 30px
            font-size: 30px
            font-weight: bold

        .information
            display: flex
            width: 35%
            white-space: pre-wrap
            height: 100%
            align-items: center
            align-self: center
            padding-right: 5%

        .slider
            width: 60%

</style>