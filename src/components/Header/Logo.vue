<template>
    <div id="logo">
        <img :src="picture.src" :alt="loadLogo" id="picture">
        <div id="text-block">
            <p v-for="word in titleHomeWordsArray" class="text"> {{ word }}</p>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Logo.vue",
        data(){
            return{
                link: 'https://c7.hotpng.com/preview/1009/720/961/logo-hawk-bird-bird.jpg',
                picture: Image,
                titleHomeWordsArray: ['Название', 'Сайта'],
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
            }
        }
    }
</script>

<style scoped>
    #logo {
        display: flex;
        flex-direction: row;
        width: 20%;
        margin: 0;
        justify-content: center;
        flex-wrap: wrap;
    }

    #picture{
        text-align: center;
        object-fit: contain;
        height: 100%;
        border-radius: 50%;
    }

    #text-block {
        display: flex;
        color: white;
        font-size: 20px;
        font-family: futura book c,Arial,sans-serif;
        margin: 0 auto 0 10px;
        flex-direction: column;
        justify-content: center;
    }
</style>