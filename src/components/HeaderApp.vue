<script>
export default {
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
<header class="navbar">
    <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="">
    </div>
    <div class="options">
        <ul class="options-list">
            <li class="list-item" v-for="(option, index) in navOptions" key="option.option"><a href="">{{ option.option }}</a></li>
        </ul>
    </div>
</header>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

.navbar {
    @include flex(row, space-between, center);
    height: 70px;
    width: 70%;
    margin: 0 auto;
    .logo {
        @include flex(row, space-between, center);
        height: 100%;
        img {
            height: 80%;
            cursor: pointer;
        }
    }

    .options{
        height: 100%;
        @include flex(row, space-between, center);

        .options-list {    
            @include flex(row, space-between, center);
            list-style-type: none;
            color: $secondary_color;
            font-size: .6rem;
            font-weight: 700;
            gap: .6rem;
            text-transform: uppercase;
            height: 100%;
        }

        .list-item {
            line-height: 66px;
            a {
                text-decoration: none;
                color: inherit;
            }
        }
        .list-item:hover {
            border-bottom: 1px solid lightskyblue;
            color: $primary_color;
            animation-name: border;
            animation-duration: 1.2s;
            animation-timing-function: linear;
            animation-iteration-count: infinite;
        }
    }
}

@keyframes border {
    25% {
        border-bottom: 3px solid lightskyblue;
    }

    50% {
        border-bottom: 5px solid $primary_color;
    }

    75% {
        border-bottom: 3px solid lightskyblue;
    }
}


</style>
