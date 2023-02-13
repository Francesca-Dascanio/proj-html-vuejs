<script>

export default {
    name: 'AppHeader',
    data () {
        return {

        }
    }
}

</script>

<template>

    <header>
        <!-- In container-lg andrà background-image -->
        <div class="container-lg">
            <div class="header-top container-sm">
                <nav class="flex space-btw">
                    <div class="logo">
                        LOGO
                    </div>
                    <div class="menu">
                        MENU
                    </div>

                </nav>
            </div>
            <div class="header-bottom container-sm">
                <div class="box flex align-items py-lg">
                    <div class="info">
                        <h1 class="py-md">
                            MAIN TITLE
                        </h1>
                        <hr>
                        <p class="py-md">
                            Lorem ipsum, dolor sit amet consectetur adipisicing elit. Odit, obcaecati.
                        </p>
                        <button>
                            Button
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
    background-color: lightblue;

    .header-top {
        background-color: yellow;
    }

    .header-bottom {
        background-color: orange;

        .box {
            .info {
                hr {
                    border-width: 0.5px;
                    border-style: solid;
                    width: 20%;
                }

                button {
                    @include button ($primary-color, $fourth-color)
                }
            }
        }
    }
}

</style>
