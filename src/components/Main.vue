<template>
    <div id="body">
        <Registration />
    </div>
</template>

<script>
    import Registration from "@/components/Main/Registration.vue";
    export default {
        name: "Main",
        components: {Registration}
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