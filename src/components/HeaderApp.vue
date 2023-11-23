<script>
export default {

    components: {},

    data() {
        return {
            navOptions: [
                {
                    option: 'Characters'
                },
                {
                    option: 'Comics'
                },
                {
                    option: 'Movies'
                },
                {
                    option: 'Tv'
                },
                {
                    option: 'Games'
                },
                {
                    option: 'Collectibles'
                },
                {
                    option: 'Videos'
                },
                {
                    option: 'Fans'
                },
                {
                    option: 'News'
                },
                {
                    option: 'Shop'
                }
            ]
        }
    },
    methods: {},
}

</script>

<template>
<div class="navbar">
    <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
    </div>
    <div class="options">
        <ul>
            <li v-for="(option, index) in navOptions" key="option.option">{{ option }}</li>
        </ul>
    </div>
</div>
</template>

<style lang="scss" scoped>

</style>
