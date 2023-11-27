<script>
export default {
    props: {
        image: String,
        price: String,
        series: String,
        type: String,
    },

    data() {
        return {

        }
    }
}
</script>

<template>
    <div class="col">
        <img :src="image" :alt="series">
        <span class="title">{{ series }}</span>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

.col {
    width: calc(100% / 6) - 2%;
    height: 35%;

    img {
        height: 90%;
        display: block;
        aspect-ratio: 1;
        object-fit: cover;
        object-position: top;
        margin-bottom: .6rem;
    }

    .title {
        display: block;
        color: $white_color;
        text-transform: uppercase;
        font-size: .6rem;
        margin: .7rem 0;
    }
}
</style>