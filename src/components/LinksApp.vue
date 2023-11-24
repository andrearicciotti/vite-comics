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
            <div class="product flex" v-for="product in products" key="product.imagePath">
                <img :src="product.imagePath" :alt="product.title">
                <span>{{ product.title }}</span>
            </div>
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
            height: 100%;
            padding: 1rem;
            font-size: .5rem;
            text-transform: uppercase;

            img {
                height: 60%;
                margin-right: .6rem
                
            }
        }
    }
}

.flex {
    @include flex(row, space-between, center);
}


</style>
