<template lang="pug">
    div(id="menu")
        a(
            v-for="button in buttons"
            :href="`#${button.anchor}`"
            :id="`new${button.anchor}`"
            @mouseover="over(button.title)"
            @mouseleave="leave(button.title)"
        ) {{button.title}}
</template>

<script>
    export default {
        name: "Menu",
        props: {
            buttons: Array,
            menuHide: Function,
            menuAppearance: Function,
        },
        methods: {
            over(title){
                if(title === "Контакты"){
                    this.menuAppearance();
                }
            },
            leave(title){
                if(title === "Контакты"){
                    this.menuHide();
                }
            }
        }
    }
</script>

<style lang="sass" scoped>
    #menu
        display: flex
        flex-direction: row
        width: 50%
        margin: 0 5% 0 5%
        height: 100%
        color: white

        a
            color: white
            display: flex
            align-items: center
            flex: 1
            justify-content: center
            text-decoration: none
            height: 100%
            font-size: 20px

        a:hover
            background: #2a2a2a

</style>