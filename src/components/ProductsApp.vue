<script>
export default {
    data () {
        return {
            products: [
                {
                    title: 'digital comics',
                    imagePath: '../src/assets/img/buy-comics-digital-comics.png'
                },
                {
                    title: 'cd merchandise',
                    imagePath: '../src/assets/img/buy-comics-merchandise.png'
                },
                {
                    title: 'subscription',
                    imagePath: '../src/assets/img/buy-comics-subscriptions.png'
                },
                {
                    title: 'comic shop locator',
                    imagePath: '../src/assets/img/buy-comics-shop-locator.png'
                },
                {
                    title: 'dc power visa',
                    imagePath: '../src/assets/img/buy-dc-power-visa.svg'
                }
            ]
        }
    }
}
</script>

<template>
    <section class="products">
        <div class="flex-container">
            <a href="" class="product flex" v-for="product in products" key="product.imagePath">
                <img :src="product.imagePath" :alt="product.title">
                <span>{{ product.title }}</span>
            </a>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;
.products {
    background-color: $primary_color;
    color: $white_color;
    width: 100%;
    height: 90px;
    .flex-container {
        width: 70%;
        height: 100%;
        margin: 0 auto;
        @include flex(row, space-between, center);
        .product {
            width: calc(100% / 5);
            height: 100%;
            text-decoration: none;
            color: inherit;
            font-size: .6rem;
            text-transform: uppercase;
            gap: .4rem;
            
            &.flex {
                @include flex(row, center, center);
            }
            
            img {
                height: 35%;
            }
        }
    }
}



</style>
