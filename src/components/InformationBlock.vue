<template lang="pug">
    div(id="information-block")
        div(id="image-block")
            img(:src="picture.src" :alt="getImage" id="image")
        div(id="info-block")
            h4(id="title") {{title | uppercase}}
            div(id="price") {{price | priceFilter}}
            div(id="brief-information") {{briefInformation}}
            div(id="block-date")
                div(id="start") {{startDate}}
                div(id="dates")
                    div(id="date" v-for="date in dates") {{date}}
</template>

<script>
    export default {
        name: "InformationBlock",
        props: {
            link: String,
            title: String,
            price: String,
            briefInformation: String,
            dates: Array,
        },
        data(){
            return{
                picture: Image,
                startDate: 'Ближайшие даты:',
            }
        },
        computed: {
            getImage(){
                let image = new Image();

                image.onload = () => {
                    this.picture = image;
                }

                image.src = this.link;
                return 'image download';
            }
        },
        filters:{
            uppercase(text) {
                return text.toUpperCase();
            },
            priceFilter(text){
                return text + 'руб';
            }
        }
    }
</script>

<style lang="sass" scoped>
    #information-block
        display: flex
        flex-direction: row
        width: 80%
        height: auto
        padding: 1% 1% 0 1%
        margin: 0 10% 0 10%
        border-bottom: 1px solid #DEDFE2
        box-sizing: border-box

        #image-block
            display: flex
            width: 15%
            padding: 5% 1% 5% 1%
            border-right: 1px solid #DEDFE2

            #image
                width: 100%
                object-fit: contain

        #info-block
            display: flex
            flex-direction: row
            flex-wrap: wrap
            justify-content: space-between
            width: 80%
            padding: 5% 5% 1% 5%
            color: black

            #title
                color: inherit
                float: left
                flex-basis: 80%

            #price
                flex-wrap: nowrap
                color: inherit
                float: right
                flex-basis: 20%
                font-family: roboto,Arial,sans-serif
                font-size: 23px

            #brief-information
                color: inherit
                float: left
                margin-top: 5%
                flex-basis: 100%

            #block-date
                display: flex
                flex-direction: row
                color: black
                width: 100%
                margin-top: 3%
                align-content: flex-end

                #start
                    color: inherit
                    height: 100%
                    width: 30%

                #dates
                    color: inherit
                    display: flex
                    flex-direction: column
                    width: 70%

                    #date
                        color: inherit
                        margin: 0 auto 5px 0
</style>