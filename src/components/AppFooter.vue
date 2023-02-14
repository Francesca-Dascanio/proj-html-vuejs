<script>

export default {
    name: 'AppFooter',
    props: {
        footerContact: Object
    }
}

</script>

<template>
    <footer>
        <div class="container-lg">
            <div class="footer-top container-sm">
                <div class="cards flex">
                    <div class="card">
                        Card 1
                    </div>
                    <div class="card">
                        Card 2
                    </div>
                    <div class="card">
                        Card 3
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
.container-lg {

    background-color: lightblue;
    .footer-top {

        background-color: yellow;
        .cards {
            width: 100%;

            .card {
                width: calc(100% / 3);
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
