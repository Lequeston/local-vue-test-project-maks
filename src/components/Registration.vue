<template lang="pug">
    div(class="registration" id="contacts")
        div(id="legend") Связаться с нами
        form(id="input-form" method="post")
            input(
                    v-for="(name, property) in registrationName"
                    class="registration-input"
                    :placeholder="name"
                    :key="property"
                    :name="property")
            textarea(name="information" :placeholder="information" class="registration-input")
            input(type="submit" :value="buttonText" id="button")
</template>

<script>
    export default {
        name: "Registration",
        props: {
            registrationName: {
                name: String,
                email: String,
                numberPhone: String,
            },
            information: String,
            buttonText: String
        }
    }
</script>

<style lang="sass" scoped>
    .registration
        display: flex
        flex-direction: column
        margin: 5% 25% 0 25%
        width: 50%
        height: 760px
        border: 3px solid slategray
        box-sizing: content-box
        text-align: center
        padding: 5% 0 5% 0

        #legend
            color: black
            font-size: 36px
            font-weight: 600

        #input-form
            display: flex
            flex-direction: column
            padding: 5% 5% 0 5%
            height: 100%

            .registration-input
                border: 1px solid #d6d6d6
                border-top: 0
                border-left: 0
                border-right: 0
                height: 70px
                font-size: 20px
                margin: 5% 0 5% 0
                color: lightgray

            .registration-input:valid
                color: black


            #button
                color: lightgray
                width: 320px
                height: 60px
                opacity: 0.3
                padding: 5px 15px
                border: 1px solid #3857dc
                border-radius: 100px
                float: right
                text-decoration: none
                font-family: Helvetica
                font-size: 14px
                color: #3857dc
                letter-spacing: 0
                line-height: 21px
                text-align: center
                margin: 5% auto 0 auto

            #button:hover
                background: #3857dc
                color: #FFFFFF
                letter-spacing: 0
                line-height: 21px
</style>