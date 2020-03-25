<template>
    <div id="body">
        <InformationBlock
                v-for="info in informationBlocks"
                :key="info.id"
                v-bind="getInfo(info)"
        />
        <Registration />
        <GeneralInformation />
    </div>
</template>

<script>
    import Registration from "@/components/Registration.vue";
    import InformationBlock from "@/components/InformationBlock.vue";
    import GeneralInformation from "@/components/GeneralInformation.vue";
    export default {
        name: "Main",
        components: {GeneralInformation, InformationBlock, Registration},
        data(){
            return{
                informationBlocks: [
                    {
                        id: 0,
                        link: 'https://uprav.ru/crop/w170h134/85/upload/iblock/36f/36f862757b787d544a512ee7e63ed1dc.jpg',
                        title: 'директор компании',
                        price: '47 175',
                        briefInformation: 'Повышение квалификации, 40 ак. часов',
                        dates: ['30 марта - 03 апреля 2020 — Москва',
                            '04-08 мая 2020 — Санкт-Петербург'],
                    },
                    {
                        id: 1,
                        link: 'https://uprav.ru/crop/w170h134/85/upload/iblock/36f/36f862757b787d544a512ee7e63ed1dc.jpg',
                        title: 'директор компании',
                        price: '47 175',
                        briefInformation: 'Повышение квалификации, 40 ак. часов',
                        dates: ['30 марта - 03 апреля 2020 — Москва',
                            '04-08 мая 2020 — Санкт-Петербург'],
                    },
                    {
                        id: 2,
                        link: 'https://uprav.ru/crop/w170h134/85/upload/iblock/36f/36f862757b787d544a512ee7e63ed1dc.jpg',
                        title: 'директор компании',
                        price: '47 175',
                        briefInformation: 'Повышение квалификации, 40 ак. часов',
                        dates: ['30 марта - 03 апреля 2020 — Москва',
                            '04-08 мая 2020 — Санкт-Петербург'],
                    },
                    {
                        id: 3,
                        link: 'https://uprav.ru/crop/w170h134/85/upload/iblock/36f/36f862757b787d544a512ee7e63ed1dc.jpg',
                        title: 'директор компании',
                        price: '47 175',
                        briefInformation: 'Повышение квалификации, 40 ак. часов',
                        dates: ['30 марта - 03 апреля 2020 — Москва',
                            '04-08 мая 2020 — Санкт-Петербург'],
                    },
                ]
            }
        },
        methods: {
            getInfo(info){
                let newInfo = {...info};
                delete newInfo.id;
                return newInfo;
            }
        }
    }
</script>

<style scoped>
    #body {
        padding: 5% 0 5% 0;
        display: flex;
        flex-direction: column;
        width: 100%;
    }
</style>