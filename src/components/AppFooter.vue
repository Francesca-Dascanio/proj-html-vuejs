<script>

export default {
    name: 'AppFooter',
    props: {
        footerContacts: Array,
        footerSocials: Array
    },
    methods: {
        scrollTop: function () {
            window.scrollTo({
            top: 0,
            left: 0,
            behavior: 'smooth'
            });
        }
    }
}

</script>

<template>
    <footer id="footer">
        <div class="container-lg">
            <!-- Inizio Footer Top -->
            <div class="footer-top container-sm">
                <div class="cards flex space-btw">
                    <div class="card flex space-btw align-items">
                        <div class="card-img">
                            <img src="/src/assets/avadabarbers_footer_shop_image-400x312.png" alt="Image">
                        </div>
                        <button>
                            SHOP OUR RANGE NOW
                        </button>
                    </div>
                    <div class="card flex align-items">
                        <div class="footer-logo">
                            <img src="/src/assets/avadabarbers-logo-x1.png" alt="Footer-Logo">
                        </div>
                        <div class="footer-contacts text-center">
                            <ul>
                                <li v-for="contact in footerContacts">
                                    <a href="#">
                                        {{ contact }}   
                                    </a>
                                </li>
                            </ul>
                        </div>
                        <div class="footer-socials">
                            <ul class="flex">
                                <li v-for="social in footerSocials">
                                    <a href="#">
                                        <font-awesome-icon :icon="social" />
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="card flex align-items space-btw">
                        <div class="card-img">
                            <img src="/src/assets/avadabarbers_footer_appointment_image-400x312.png" alt="Image">
                        </div>
                        <button @click="$emit('getOn')">
                            BOOK AN APPOINTMENT
                        </button>
                    </div>
                </div>
            </div>

             <!-- Inizio Footer Bottom -->
            <div class="footer-bottom container-lg">
                <p class="container-sm text-center py-md">
                    &#169; Copyright 2012 - 2020 | Avada Theme By ThemeFusion | All Rights Reserved | Powered by Vite + Vue
                </p>
                <button class="container-md text-right" @click="scrollTop()">
                    <font-awesome-icon icon="fa-solid fa-chevron-up" />
                </button>
            </div>
        </div>
    </footer>

</template>

<style lang="scss" scoped>
@import '../styles/partials/variables.scss';
@import '../styles/partials/mixins.scss';
.container-lg {

    background-color: $fourth-color;
    .footer-top {
        .cards {
            width: 100%;
            padding: 2rem 0;

            .card {
                width: calc(100% / 4);
                flex-direction: column;

                .card-img {
                    width: 80%;

                    img {
                        width: 100%;
                    }
                }

                .footer-logo {
                    width: 60%;

                    img {
                        width: 100%;
                    }
                }

                .footer-contacts {
                    padding: 2rem 0;

                    ul {
                        list-style: none;

                        li {

                            a {
                                @include a ($secondary-color);
                                font-size: 0.8rem;
                            }
                        }
                    }
                }

                .footer-socials {
                    ul {
                        list-style: none;

                        li {
                            padding: 0.5rem;

                            a {
                                @include a ($secondary-color);
                                font-size: 0.8rem;
                            }
                        }
                    }


                }

                button {
                    @include button;
                }
            }
        }
    }

    .footer-bottom {
        background-color: $sixth-color;
        position: relative;
        left: 0;
        top: 0;

        button {
            position: absolute;
            right: 0;
            bottom: 0;
            color: $third-color;
            border-style: none;
            background-color: transparent;
            border: 1px solid $sixth-color;

            > * {
                background-color: $seventh-color;
                padding: 0.5rem;
                border-radius: 5px 5px 0 0;
            }
        }
    }
}

</style>
