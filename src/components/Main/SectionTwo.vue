<script>

export default {
    name: 'SectionTwo',
    data () {
        return {
            services: [
                {
                    service: 'Trim & Cut',
                    description: 'Avada Barbers are experts in the lickety split trim and hair cut. Quick but careful and ridiculously good looking.',
                    image: 'avadabarbers-trimcut-icon-before.png'
                },
                {
                    service: 'Wash & Dry',
                    description: 'Take a seat in our fine leather chairs, lean back and let us lather you a fresh head in a luxury fashion.',
                    image: 'avadabarbers-washndry-icon.png'
                },
                {
                    service: 'Beard Tidy',
                    description: 'Tame the tangles and untidy facial hairs like a gentleman with our Beard Tidy services from Avada Barbers.',
                    image: 'avadabarbers-beardtrim-icon.png'
                }
            ]
        }
    }
    
}

</script>

<template>
    <section id="section-2">
        <div class="container-lg">
            <div class="container-sm">
                <div class="section-title text-center py-md">
                    <h5>
                        MENS GROOMING SERVICES
                    </h5>
                    <h2>
                        Services
                    </h2>
                </div>

                <div class="section-contents flex align-items py-md">
                    <div class="cards flex space-btw">
                        <div class="card text-center py-md" v-for="item in services">
                            <div class="card-img">
                                <img :src="`/src/assets/${item.image}`" alt="Icon">
                            </div>
                            <h3>
                               {{ item.service }}
                            </h3>
                            <p>
                                {{ item.description }}
                            </p>
                        </div>
                        <!-- <div class="card text-center py-md">
                            Card 2
                        </div>
                        <div class="card text-center py-md">
                            Card 3
                        </div> -->
                    </div>

                    <button>
                        READ ABOUT OUR SERVICES
                    </button>
                </div>
            </div>
            <div class="container-lg triangle">
                <svg class="fusion-big-triangle-candy" xmlns="http://www.w3.org/2000/svg" version="1.1" width="100%" height="60px" viewBox="0 0 100 100" preserveAspectRatio="none" style="fill:#000000;padding:0;"><path d="M0 100 L50 2 L100 100 Z"></path></svg>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '/src/styles/main.scss' as *;

#section-2 {
    .container-lg {
        .container-sm {

            padding: 2rem 0 4rem 0;
            
            .section-contents {
                flex-direction: column;

                .cards {

                    width: 100%;
                    .card {
                        width: calc(100% / 4);

                        > * {
                            padding-bottom: 1rem;

                        }

                        // > .card-img {
                        //     width: 80%;
                        //     height: 100%;
                        // }

                        > p {
                            padding: 0 1rem 1rem;
                            font-size: 0.8rem;
                        }
                    
                    }
                }

                button {
                    @include button;
                }
            }
        }

        .triangle {
            width: 100%;
            height: 60px;

        }
    }
}


</style>
