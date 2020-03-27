<template lang="pug">
    div(id="logo")
        img(:src="picture.src" :alt="loadLogo" id="picture")
        div(id="text-block")
            p(v-for="word in titleHomeWordsArray" class="text") {{ word }}
</template>

<script>
    export default {
        name: "Logo.vue",
        props:{
            link: String,
            title: String,
        },
        data(){
            return{
                picture: Image,
            }
        },
        computed: {
            loadLogo(){
                let image = new Image();

                image.onload = () => {
                    this.picture = image;
                }

                image.src = this.link;
                return 'image download';
            },
            titleHomeWordsArray(){
                let {title} = this;
                return (title !== undefined) ? title.split(' ') : [];
            }
        }
    }
</script>

<style lang="sass" scoped>
    #logo
        display: flex
        flex-direction: row
        width: 20%
        margin: 1% 0 1% 0
        justify-content: center
        flex-wrap: nowrap
        color: white

        #picture
            text-align: center
            object-fit: contain
            height: 100%
            border-radius: 50%

        #text-block
            display: flex
            color: white
            font-size: 20px
            font-family: futura book c,Arial,sans-serif
            margin: 0 auto 0 10px
            flex-direction: column
            justify-content: center
</style>