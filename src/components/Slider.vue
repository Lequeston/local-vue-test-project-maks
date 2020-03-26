<template lang="pug">
    div(class="slider")
        button(class="button left-button" v-on:click="onButtonLeftClick")
        img(class="image" :src="picture.src" :alt="loadImage(imageIndex)")
        button(class="button right-button" v-on:click="onButtonRightClick")
</template>

<script>
    export default {
        name: "Slider",
        data(){
            return{
                imageIndex: 0,
                picture: Image,
                pictures: [],
                arrayImages: [
                    'https://avatars.mds.yandex.net/get-pdb/1369887/746dace4-efdb-4d53-a060-8de410e4d408/s1200?webp=false',
                    'https://avatars.mds.yandex.net/get-pdb/1043578/1e859f55-f1de-44f5-b66b-4a0f5e2dc455/s1200?webp=false',
                    'http://alenatv.kiev.ua/wp-content/uploads/2016/10/9N1A9002_1.jpg',
                ]
            }
        },
        methods: {
            onButtonLeftClick(e){
                this.imageIndex = (this.imageIndex + 1) % this.arrayImages.length;
            },

            onButtonRightClick(e){
                this.imageIndex = (this.imageIndex === 0) ?  (this.arrayImages.length - 1) : (this.imageIndex - 1);
            },

            loadImage(index){
                if (this.pictures[index] == undefined){
                    let image = new Image();

                    image.onload = () => {
                        this.picture = image;
                        this.picture[index] = image;
                    }

                    image.src = this.arrayImages[index];
                    return 'image download';
                } else {
                    this.picture = this.picture[index];
                    return 'image'
                }
            }
        }
    }
</script>

<style lang="sass" scoped>
    .slider
        width: 700px
        height: auto
        display: flex
        flex-direction: row
        align-items: center

        .button
            display: flex
            justify-content: center
            align-items: center
            width: 30px
            height: 50px
            background: white
            border: none
            color: #424242
            font-size: 50px
            font-weight: bold

        .button:hover
            color: black

        .left-button:after
            content: '\003C'

        .right-button:after
            content: '\003E'

        .image
            width: 100%
            height: auto
            object-fit: cover
            margin: 0 10px 0 10px
</style>