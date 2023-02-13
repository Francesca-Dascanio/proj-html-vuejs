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
                    <h5>
                    Lorem ipsum dolor sit.
                    </h5>
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
                        <h5>
                        Lorem ipsum dolor sit.
                        </h5>
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
            <!-- Div contenitore di entrambe le sotto-sezioni della section-3 -->
            <div class="container-lg">
                <div class="sub-section-a container-lg">
                    <div class="section-title text-center py-md">
                        <h5>
                        Lorem ipsum dolor sit.
                        </h5>
                        <h2>
                            SECTION 3 TITLE
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
                            <div class="card text-center py-md">
                                Card 4
                            </div>
                        </div>
                        <button class="mb-lg">
                            Button
                        </button>
                    </div>
                </div>
                <div class="sub-section-b">
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

// ATTENZIONE: altezze di prova 
#section-3 {
    .container-lg {
    background-color: lightblue;
    position: relative;
    top: 0;
    left: 0;

        .sub-section-a {
            background-color: pink;

                .section-contents {
                    flex-direction: column;

                    .cards {
                        width: 100%;
                        .card {
                            width: calc(100% / 4);
                        }
                    }
                }
        }

        .sub-section-b {
            background-color: fuchsia;
            position: absolute;
            width: 1100px;
            left: 50%;
            transform: translate(-50%);
            top: 90%;

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
