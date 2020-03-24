<template>
    <div id="info">
        <div id="numberPhone">{{ numberPhone }}</div>
        <div id="workingHours">{{ workingHours }}</div>
        <div id="town">{{ town }}</div>
    </div>
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

<style scoped>
    #info {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        flex: 1;
        width: 20%;
    }

    #numberPhone {
        color: white;
        font-family: futura medium c,Arial,sans-serif;
        font-size: 20px;
    }

    #workingHours {
        color: white;
        font-family: futura medium c,Arial,sans-serif;
        font-size: 15px;
    }

    #town {
        color: white;
        font-family: futura medium c,Arial,sans-serif;
        font-size: 15px;
    }
</style>