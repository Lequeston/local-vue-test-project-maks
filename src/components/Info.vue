<template lang="pug">
    div(id="info")
        div(id="numberPhone") {{ numberPhone }}
        div(id="workingHours") {{ workingHours }}
        div(id="town") {{ town }}
</template>

<script>
    export default {
        name: "Info",
        data(){
            return{
                numberPhone: '8(800)553-53-55',
                workingHours: 'Пн.-Пт.: 8:00-19:00',
                town: 'Москва',
            }
        }
    }
</script>

<style lang="sass" scoped>
    #info
        display: flex
        flex-direction: column
        justify-content: space-between
        flex: 1
        width: 20%
        color: white

        #numberPhone
            font-size: 20px

        #workingHours
            font-size: 15px

        #town
            font-size: 15px
</style>