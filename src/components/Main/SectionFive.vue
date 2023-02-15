<script>

export default {
    name: 'SectionFive',
    data () {
        return {
            posts: [
                {
                    name: 'Avada Barbers Now Open',
                    abstract: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt inventore dolor nulla explicabo sed consequatur.',
                    image: 'avadabarbers-choosing-blog-700x441.jpg'
                },
                {
                    name: 'Choosing The Right Barber',
                    abstract: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt inventore dolor nulla explicabo sed consequatur.',
                    image: 'avadabarbers-second-blog-700x441.jpg'
                },
                {
                    name: 'Quick Service Guide',
                    abstract: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Deserunt inventore dolor nulla explicabo sed consequatur.',
                    image: 'avadabarbers-ourservice-blog-700x441.jpg'
                },

            ]
        }
    }
    
}

</script>

<template>
    <section id="section-5">
        <div class="container-lg">
            <div class="container-lg triangle">
                <svg class="fusion-big-triangle-candy" xmlns="http://www.w3.org/2000/svg" version="1.1" width="100%" height="60px" viewBox="0 0 100 100" preserveAspectRatio="none" style="fill:#ffffff;padding:0;"><path d="M0 100 L50 2 L100 100 Z"></path></svg>
            </div>
            <div class="container-sm">
                <div class="section-title text-center py-md">
                    <h5>
                        TALES FROM OUR BARBER SHOP
                    </h5>
                    <h2>
                        Recent Blog Posts
                    </h2>
                </div>

                <div class="section-contents flex align-items py-md">
                    <div class="cards flex space-btw align-items">
                        <div class="card text-center py-md" v-for="item in posts">
                            <div class="card-img">
                                <img :src="`/src/assets/${item.image}`" alt="Icon">
                            </div>
                            <div class="card-contents">
                                <h3>
                                    {{ item.name }}
                                </h3>
                                <p>
                                    {{ item.abstract }}
                                </p>
                            </div>
                        </div>
                    </div>

                    <button>
                        READ MORE FROM OUR BLOG
                    </button>
                </div>
            </div>

        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '/src/styles/main.scss' as *;

#section-5 {
    .container-lg {
    background-color: $fifth-color;

        .triangle {
            width: 100%;
            height: 60px;

                svg {
                    transform: rotate(180deg);
                }
        }
        .container-sm {
            padding: 3rem 0;
            .section-contents {
                flex-direction: column;

                .cards {
                    width: 100%;
                    .card {
                        width: calc(100% / 4);

                        > * {
                            padding-bottom: 1rem;

                        }

                        > .card-img {

                             img {
                                width: 100%;
                                object-fit: cover;
                             }
                        }

                        > .card-contents {
                            width: 100%;
                        }

                    }

                }

                button {
                        @include button ($third-color);
                    }
            }
        }
    }
}


</style>
