<script>

export default {
    name: 'AppHeader'
}

</script>

<template>

    <header>
        <!-- In container-lg andrà background-image -->
        <div class="container-lg">
            <div class="header-top container-sm">
                <nav class="flex space-btw align-items">
                    <div class="logo">
                        <img src="../assets/avadabarbers-logo-x2-200x70.png" alt="Avada Barbers">
                    </div>
                    <div class="menu" @click="$emit('getClick')">
                        <font-awesome-icon icon="fa-solid fa-cart-shopping" />
                        <font-awesome-icon icon="fa-solid fa-bars" />
                    </div>

                </nav>
            </div>
            <div class="header-bottom container-sm">
                <div class="box flex align-items py-lg">
                    <div class="info">
                        <h1 class="py-md">
                            Barber Shop
                        </h1>
                        <hr>
                        <h5 class="py-md">
                            The Pinnacle of Male Grooming
                        </h5>
                        <button>
                            LEARN MORE
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </header>

</template>

<style lang="scss" scoped>
@import '../styles/partials/variables.scss';
@import '../styles/partials/mixins.scss';
.container-lg {
    background-image: url('../assets/avadabarbers-homepage-hero-bg.jpg');
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;

    .header-top {
        // background-color: black;
        .logo {
            width: 150px;

            img {
                width: 100%;
                padding: 1rem 0;
            }
        }

        .menu {
            color: $fifth-color;
            
            > * {
                margin-left: 20px;
                padding: 1rem 0 1rem 1rem;
            }
        }
    }

    .header-bottom {
        // background-color: black;
        .box {

            padding: 6rem 0;
            .info {
                h1 {
                    font-size: 3.5rem;
                    color: $fifth-color;
                }

                hr {
                    border-width: 1px;
                    border-style: solid;
                    width: 20%;
                    color: $primary-color;
                }

                h5 {
                    color: $secondary-color;
                    font-weight: lighter;
                }

                button {
                    @include button ($primary-color, $fourth-color)
                }
            }
        }
    }
}

</style>
