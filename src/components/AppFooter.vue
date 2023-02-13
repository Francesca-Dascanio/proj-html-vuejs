<script>

export default {
    name: 'AppFooter',
    data () {
        return {

        }
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
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo dolores voluptas ab blanditiis nam sunt?
                </p>
                <div class="container-md text-right">
                    Bottone
                </div>
            </div>
        </div>
    </footer>

</template>

<style lang="scss" scoped>

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
        background-color: orange;
    }
}

</style>
