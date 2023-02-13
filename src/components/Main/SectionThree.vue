<script>

export default {
    name: 'SectionThree',
    
}

</script>

<template>
    <section id="section-3">
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
    background-color: lightblue;
    height: calc(100% - 30px);

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
