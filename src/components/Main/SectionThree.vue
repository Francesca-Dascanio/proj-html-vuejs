<script>

export default {
    name: 'SectionThree',
    data () {
        return {
            products: [
                {
                    product: 'Brush',
                    price: '$ 15.00',
                    image: 'brush_dark.png'
                },
                {
                    product: 'Scissors',
                    price: '$ 85.00',
                    image: 'scissors.png'
                },
                {
                    product: 'Hot Oil',
                    price: '$ 15.00',
                    image: 'hot_oil_dark.png'
                },
                {
                    product: 'Straight Razor',
                    price: '$ 30.00',
                    image: 'straight_razor_dark.png'
                }
            ]
        }
    }
    
}

</script>

<template>
    <section id="section-3">
        <div class="container-lg">
            <div class="sub-section-a container-lg">
                <div class="section-title text-center py-md">
                    <h5>
                        WE HAVE YOU COVERED
                    </h5>
                    <h2>
                        Avada Grooming Products
                    </h2>
                </div>

                <div class="section-contents flex align-items py-md">
                    <div class="cards flex space-btw align-items">
                        <div class="card text-center py-md" v-for="item in products">
                            <div class="card-img">
                                <img :src="`/src/assets/${item.image}`" alt="Icon">
                            </div>
                            <div class="card-contents">
                                <h3>
                                    {{ item.product }}
                                </h3>
                                <p>
                                    {{ item.price }}
                                </p>
                            </div>
                        </div>
                    </div>
                    <button class="mb-lg">
                        SHOP OUR PRODUCT RANGE
                    </button>
                </div>
            </div>
            <div class="sub-section-b container-sm">
                <div class="sub-section-b-container flex">
                    <div class="sub-section-b-img flex justify-center align-items">
                        <div class="img-container">
                            <img src="/src/assets/shaving_butter.png" alt="Shaving Butter" />
                        </div>
                    </div>

                    <div class="sub-section-b-contents py-md">
                        <h5>
                            THIS MONTHS FEATURED PRODUCT
                        </h5>
                        <h2>
                            Shaving Butter
                        </h2>
                        <p class="py-md">
                            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempora enim, inventore aspernatur nisi sint eius quibusdam dicta corporis repellendus aut obcaecati dolore, dolorem consequuntur debitis deleniti quidem atque suscipit quas deserunt omnis animi voluptas eos.
                        </p>
                        <button>
                            BUY NOW
                        </button>
                    </div>
                </div>
            </div>
        </div>
    </section>  
</template>

<style lang="scss" scoped>
@use '/src/styles/main.scss' as *;

#section-3 {
    .container-lg {

        .sub-section-a {
            // height: calc(100% - 30px);
            background-image: url('/src/assets/avadabarbers-reviewsbackground.jpg');
            background-size: cover;
            background-position: center;
            background-repeat: no-repeat;
            padding-bottom: 4rem;

                .section-contents {
                    flex-direction: column;

                    .cards {
                        width: 100%;
                        height: 90%;
                        .card {
                            width: calc(100% / 5);

                            > * {
                            padding-bottom: 1rem;

                            }

                            > .card-img {

                                height: 70%;

                                img {
                                    
                                    height: 200px;
                                    object-fit: cover;
                                }
                            }

                            > .card-contents {

                                height: 30%;

                                p {
                                    font-size: 0.8rem;
                                    color: $primary-color;
                                }
                            }
                        }
                    }

                    button {
                        @include button;
                        height: 10%;
                    }
                }
        }

        .sub-section-b {
            transform: translateY(-2rem);

                .sub-section-b-container {
                    border-top: 2px solid $primary-color;
                    .sub-section-b-img {
                        width: 30%;
                        background-image: url('/src/assets/avadabarbers-second-blog-700x441.jpg');
                        background-position: center;
                        background-size: cover;
                        background-repeat: no-repeat;
                        filter: grayscale(1);

                            .img-container {
                                img {
                                    width: 100%;
                                }
                            }
                    }

                    .sub-section-b-contents {
                        width: 70%;
                        padding: 2rem;
                        background-color: $fourth-color;

                        > p {
                            font-size: 0.8rem;
                            color: $secondary-color;
                        }

                        > button {
                            @include button;
                        }
                    }

                }

        }
    }
}

</style>
