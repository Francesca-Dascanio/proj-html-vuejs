<script>

export default {
    name: 'AppHeader'
}

</script>

<template>
    <header id="header">
        <div class="container-lg">
            <!-- Inizio Header Top -->
            <div class="header-top container-sm">
                <nav class="flex space-btw align-items">
                    <div class="logo">
                        <img src="../assets/avadabarbers-logo-x2-200x70.png" alt="Avada Barbers">
                    </div>
                    <div class="menu">
                        <ul class="flex">
                            <li>
                                <a href="#">
                                    <font-awesome-icon icon="fa-solid fa-cart-shopping" />
                                </a>
                            </li>
                            <li>
                                <a href="#" @click="$emit('getClick')">
                                    <font-awesome-icon icon="fa-solid fa-bars" />
                                </a>
                            </li>
                        </ul> 
                    </div>
                </nav>
            </div>

             <!-- Inizio Header Bottom -->
            <div class="header-bottom container-sm">
                <div class="box flex space-btw align-items">
                    <div class="info">
                        <h1>
                            Barber Shop
                        </h1>
                        <hr>
                        <p class="py-md">
                            The Pinnacle of Male Grooming
                        </p>
                        <button>
                            LEARN MORE
                        </button>
                    </div>
                    <div class="img-container">
                        <img src="../assets/avadabarbers_hero_focalmirror-400x550.png" alt="Barber">
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
    @include bg-image ('../assets/avadabarbers-homepage-hero-bg.jpg', center);

    .header-top {        
        .logo {
            width: 150px;

            img {
                width: 100%;
                padding: 1rem 0;
            }
        }

        .menu {
            ul {
                
                list-style: none;

                    li {
                        a {
                            @include a ($third-color);
                            margin-left: 20px;
                            padding: 1rem 0 1rem 1rem;
                        }
                    }
                }
        }
    }

    .header-bottom {
        .box {
            .info {

                padding-bottom: 5rem;
                width: 60%;

                h1 {
                    font-size: 4rem;
                    color: $fifth-color;
                }

                hr {
                    border-width: 1px;
                    border-style: solid;
                    width: 30%;
                    color: $primary-color;
                }

                button {
                    @include button;
                }
            }

            .img-container {
                width: 40%;

                img {
                    width: 100%;
                }
            }
        }
    }
}

</style>
