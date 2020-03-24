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
                link: 'https://banner2.cleanpng.com/20181106/icw/kisspng-google-chrome-app-computer-icons-web-browser-porta-chrome-svg-png-icon-free-download-318446-onli-5be2620f1e42f7.002521951541562895124.jpg',
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