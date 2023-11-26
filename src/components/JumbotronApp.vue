<script>
export default {
    data() {
        return {
            
        }
    }
}
</script>

<template>
    <section class="jumbotron">
        <span class="info">current series</span>
    </section>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;
.jumbotron {
    background-image: url(../assets/img/jumbotron.jpg);
    background-size: cover;
    width: 100%;
    height: 300px;
    position: relative;

    .info {
        display: block;
        position: absolute;
        background-color: $primary_color;
        color: $white_color;
        padding: .7rem;
        text-transform: uppercase;
        left: 15%;
        bottom: -5%;
    }
}
</style>
