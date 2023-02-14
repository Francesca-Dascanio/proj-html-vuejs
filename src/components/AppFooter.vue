<script>

export default {
    name: 'AppFooter',
    props: {
        footerContacts: Array
    }
}

</script>

<template>
    <footer>
        <div class="container-lg">
            <div class="footer-top container-sm">
                <div class="cards flex space-btw">
                    <div class="card flex align-items space-btw">
                        <div class="card-img">
                            <img src="/src/assets/avadabarbers_footer_shop_image-400x312.png" alt="Image">
                        </div>
                        <div class="card-button">
                            <button>
                                SHOP OUR RANGE NOW
                            </button>
                        </div>
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
                                <li>
                                    <a href="#">
                                        <font-awesome-icon icon="fa-brands fa-facebook" />
                                    </a>
                                </li>
                                <li>
                                    <a href="#">
                                        <font-awesome-icon icon="fa-brands fa-twitter" />
                                    </a>
                                </li>
                                <li>
                                    <a href="#">
                                        <font-awesome-icon icon="fa-brands fa-youtube" />
                                    </a>
                                </li>
                                <li>
                                    <a href="#">
                                        <font-awesome-icon icon="fa-brands fa-instagram" />
                                    </a>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <div class="card flex align-items space-btw">
                        <div class="card-img">
                            <img src="/src/assets/avadabarbers_footer_appointment_image-400x312.png" alt="Image">
                        </div>
                        <div class="card-button">
                            <button>
                                BOOK AN APPOINTMENT
                            </button>
                        </div>
                    </div>
                </div>
            </div>
            <div class="footer-bottom container-lg">
                <p class="container-sm text-center py-md">
                    &#169; Copyright 2012 - 2020 | Avada Theme By ThemeFusion | All Rights Reserved | Powered by Vite + Vue
                </p>
                <div class="btn-up container-md text-right">
                    <font-awesome-icon icon="fa-solid fa-chevron-up" />
                </div>
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
                                color: $secondary-color;
                                text-decoration: none;
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
                                color: $secondary-color;
                                text-decoration: none;
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

        p {
            padding: 1rem 0 0 0;
        }

        .btn-up {
            color: $third-color;

            > * {
                background-color: $seventh-color;
                padding: 1rem 1rem 0 1rem;
                border-radius: 5px 5px 0 0;
            }
        }
    }
}

</style>
