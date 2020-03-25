<template lang="pug">
    div(id="menu")
        a(
            v-for="(linkName, link) in linksName"
            :href="`#${link}`"
            :id="`new${link}`"
        ) {{linkName}}
</template>

<script>
    export default {
        name: "Menu",
        data(){
            return{
                linksName: {
                    information_title: 'Информация',
                    ourCourses: 'Наши курсы',
                    contacts: 'Контакты'
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