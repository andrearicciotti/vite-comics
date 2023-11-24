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
            ],
            socials: [
                {
                    social: 'facebook',
                    imagePath: '../src/assets/img/footer-facebook.png'
                },
                {
                    social: 'twitter',
                    imagePath: '../src/assets/img/footer-twitter.png'
                },
                {
                    social: 'youtube',
                    imagePath: '../src/assets/img/footer-youtube.png'
                },
                {
                    social: 'pinterest',
                    imagePath: '../src/assets/img/footer-pinterest.png'
                },
                {
                    social: 'periscope',
                    imagePath: '../src/assets/img/footer-periscope.png'
                }
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
        <section class="footer-bottom">

            <div class="container-bottom">
                <div class="cta">
                    <a href="">Sign up now!</a>
                </div>
                <div class="socials">
                    <span>follow Us</span>
                    <a href="" v-for="(social, index) in socials" key="social.social"><img :src="social.imagePath" alt=""></a>
                </div>
            </div>
    
        </section>
    </div>
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
                background-repeat: no-repeat;
                background-size: 100%;
                background-position: center;
            }
        }
        .footer-bottom {
            width: 100%;
            height: 83px;
            background-color: $footer_color;

            .container-bottom {
                color: $white_color;
                width: 70%;
                height: 100%;
                margin: 0 auto;
                @include flex (row, space-between, center);

                .cta {
                    width: 20%;
                    @include flex (row, start, center);

                    a {
                        text-decoration: none;
                        text-transform: uppercase;
                        font-size: .8rem;
                        color: inherit;
                        padding: .7rem;
                        border: 2px solid $primary_color;
                    }
                }

                .socials {
                    flex-grow: 1;
                    @include flex (row, end, center);
                    span {
                        text-transform: uppercase;
                        color: $primary_color;
                        margin: 0 1rem;
                    }
                    a {
                        padding: .5rem;

                        img {
                            height: 30px;
                        }
                    }
                }
            }
        }
    }
}
</style>