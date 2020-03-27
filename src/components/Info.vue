<template lang="pug">
    div(class="info")
        div(class="numberPhone") {{ numberPhone }}
        div(class="workingHours") {{ workingHours }}
        div(class="town") {{ town }}
</template>

<script>
    export default {
        name: "Info",
        props: {
            numberPhone: String,
            workingHours: String,
            town: String,
        },
    }
</script>

<style lang="sass" scoped>
    .info
        display: flex
        flex-direction: column
        justify-content: space-between
        flex: 1
        width: 20%
        margin: 1% 0 1% 0
        color: white

        .numberPhone
            font-size: 20px

        .workingHours
            font-size: 15px

        .town
            font-size: 15px
</style>