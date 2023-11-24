<script>
export default {
    data () {
        return {
            dc: [
                {
                    category: 'dc-comics',
                    tags: [
                        'Characters',
                        'Comics',
                        'Movies',
                        'TV',
                        'Games',
                        'Videos',
                        'News'
                    ]
                },
                {
                    category: 'shop',
                    tags: [
                        'Shop DC',
                        'Shop DC collectibles',
                    ]
                },
                {
                    category: 'dc',
                    tags: [
                        'Therms of use',
                        'Privacy policy (new)',
                        'Ad choices',
                        'Advertising',
                        'Jobs',
                        'Subscriptions',
                        'Talent workshop',
                        'CPSC Certificates',
                        'Ratings',
                        'Shop help',
                        'Contact us'
                    ]
                },
                {
                    category: 'sites',
                    tags: [
                        'DC',
                        'Mad magazine',
                        'DC Kids',
                        'DC Universe',
                        'DC Power Visa',
                    ]
                },
            ]
        }
    }
}
</script>

<template>

<footer>
    <div class="container">
        <section class="footer-top">

            <div class="navigation">

                <ul v-for="(category, index) in dc" key="category.category">
                    <h4>{{ category.category }}</h4>
                    <li v-for="(tag, index) in category.tags" key="tag"><a href="">{{ tag }}</a></li>
                </ul>

            </div>    

            <div class="logo">

            </div>

        </section>
    </div>
    <section class="footer-bottom">

    </section>
</footer>
</template>

<style lang="scss" scoped>
@use '../style/partials/variables' as *;
@use '../style/partials/mixins' as *;

footer {  
    .container {
        width: 100%;
        height: 300px;
        background-image: url('../assets/img/footer-bg.jpg');
        .footer-top {
    
            width: 70%;
            height: 100%;
            margin: 0 auto;
            background-size: cover;
            @include flex (row, space-between, center);
    
            .navigation, .logo {
                width: 45%;
                height: 100%;
            } 

            .navigation {
                @include flex (column, start, start);
                flex-wrap: wrap;
                color: $white_color;
                padding: 1.5rem 0;

                ul {
                    margin: 1rem 0;

                    h4 {
                        margin-bottom: .5rem;
                        text-transform: uppercase;
                    }

                    li {
                        list-style-type: none;

                        a {
                            text-decoration: none;
                            color: inherit;
                            font-size: .8rem;
                            font-weight: 300;
                        }
                    }
                }
            }
            .logo {
                background-image: url('../assets/img/dc-logo-bg.png');
                background-size: 100%;
                background-position: center;
            }
        }
    }
    .footer-bottom {
        width: 100%;
        height: 80px;
        background-color: $footer_color;
    }
}
</style>