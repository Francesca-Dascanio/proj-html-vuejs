<script>

export default {
    name: 'SectionFour',
    data () {
        return {
            reviews: [
                {
                    review: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Facere inventore molestiae aperiam. Quae dolor laboriosam labore rem nesciunt ad reprehenderit veritatis provident, corporis a, laudantium enim distinctio ipsam perspiciatis fugiat.',
                    reviewer: 'John Doe',
                    image: 'avadabarbers-trimcut-gallery6.jpg',
                },
                {
                    review: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Facere inventore molestiae aperiam. Quae dolor laboriosam labore rem nesciunt ad reprehenderit veritatis provident, corporis a, laudantium enim distinctio ipsam perspiciatis fugiat.',
                    reviewer: 'Pete Jones',
                    image: 'avadabarbers-trimcut-gallery7.jpg',
                },
                {
                    review: 'Lorem ipsum dolor, sit amet consectetur adipisicing elit. Facere inventore molestiae aperiam. Quae dolor laboriosam labore rem nesciunt ad reprehenderit veritatis provident, corporis a, laudantium enim distinctio ipsam perspiciatis fugiat.',
                    reviewer: 'Mark Wilson',
                    image: 'avadabarbers-trimcut-gallery3.jpg',
                }
            ]
        }
    }
    
}

</script>

<template>
    <section id="section-4">
        <div class="container-lg">
            <div class="container-sm">
                <div class="section-title text-center py-md">
                    <h5>
                        WHAT PEOPLE SAY
                    </h5>
                    <h2>
                        Review
                    </h2>
                </div>

                <div class="section-contents flex align-items py-md">
                    <div class="cards flex space-btw">
                        <div class="card text-center py-md" v-for="item in reviews">
                            <p>
                                {{ item.review }}
                            </p>
                            <div class="img-container">
                                <img :src="`/src/assets/${item.image}`" :alt="item.reviewer">
                            </div>
                            <h5>
                                {{ item.reviewer }}
                            </h5>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '/src/styles/main.scss' as *;


#section-4 {
    .container-lg {

        .container-sm {

            .section-contents {
                .cards {

                    width: 100%;
                    .card {
                        width: calc(100% / 4);

                        p {
                            padding-bottom: 1rem;
                            // height: 50%; tolta ma resta problema se lunghezza review differisce
                        }

                        .img-container {
                            display: inline-block;
                            padding: 1rem 0;
                            width: 50%;
                            border-radius: 50%;

                            img {
                                width: 100%;
                                border-radius: 50%;
                            }
                        }

                        h5 {
                            font-style: italic;
                        }
                    }
                }
            }
        }

    }
}

</style>
