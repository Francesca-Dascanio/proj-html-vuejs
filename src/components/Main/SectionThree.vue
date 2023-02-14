<script>

export default {
    name: 'SectionThree',
    data () {
        return {
            products: [
                {
                    product: 'Brush',
                    price: '$ 15.00',
                    image: 'brush_dark-200x200.png'
                },
                {
                    product: 'Scissors',
                    price: '$ 85.00',
                    image: 'scissors-200x200.png'
                },
                {
                    product: 'Hot Oil',
                    price: '$ 15.00',
                    image: 'hot_oil_dark-200x200.png'
                },
                {
                    product: 'Straight Razor',
                    price: '$ 30.00',
                    image: 'straight_razor_dark-200x200.png'
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
                    <div class="sub-section-b-img">
                        IMG
                    </div>

                    <div class="sub-section-b-contents py-md">
                        <h5>
                            Lorem ipsum dolor sit amet.
                        </h5>
                        <h2>
                            SUB-SECTION-B-TITLE
                        </h2>
                        <p class="py-md">
                            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Tempora enim, inventore aspernatur nisi sint eius quibusdam dicta corporis repellendus aut obcaecati dolore, dolorem consequuntur debitis deleniti quidem atque suscipit quas deserunt omnis animi voluptas eos.
                        </p>
                        <button>
                            Button
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
            height: calc(100% - 30px);
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
            background-color: fuchsia;
            transform: translateY(-30px);

                .sub-section-b-container {

                    .sub-section-b-img {
                        width: 30%;
                    }

                    .sub-section-b-contents {
                        width: 70%;
                    }

                }

        }
    }
}

</style>
