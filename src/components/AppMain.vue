<script>

export default {
    name: 'AppMain',
    data () {
        return {

        }
    }
}

</script>

<template>

    <main>
        <section id="section-1">
            <div class="container-lg">
                <div class="container-sm">
                <div class="section-title text-center py-md">
                    <p>
                    Lorem ipsum dolor sit.
                </p>
                <h2>
                    SECTION 1 TITLE
                </h2>
                </div>

                <div class="section-contents flex align-items py-md">
                    <button>
                        Button
                    </button>
                </div>
            </div>
            </div>
        </section>

        <section id="section-2">
            <div class="container-lg">
                <div class="container-sm">
                    <div class="section-title text-center py-md">
                        <p>
                        Lorem ipsum dolor sit.
                        </p>
                        <h2>
                            SECTION 2 TITLE
                        </h2>
                    </div>

                    <div class="section-contents flex align-items py-md">
                        <div class="cards flex">
                            <div class="card text-center py-md">
                                Card 1
                            </div>
                            <div class="card text-center py-md">
                                Card 2
                            </div>
                            <div class="card text-center py-md">
                                Card 3
                            </div>
                        </div>

                        <button>
                            Button
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <section id="section-3">
            
        </section>

        <section id="section-4">
            
        </section>

        <section id="section-5">
            
        </section>
        
    </main>

</template>

<style lang="scss" scoped>

#section-1 {
    .container-lg {
    background-color: lightblue;
        .container-sm {
            background-color: lightseagreen;

            .section-contents {
                flex-direction: column;
            }
        }
    }
}


#section-2 {
    .container-lg {
    background-color: lightblue;
        .container-sm {
            background-color: lightcoral;

            .section-contents {
                flex-direction: column;

                .cards {

                    width: 100%;
                    .card {
                        width: calc(100% / 3);
                    }
                }
            }
        }
    }
}

</style>
