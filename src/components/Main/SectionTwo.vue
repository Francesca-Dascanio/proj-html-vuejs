<script>

export default {
    name: 'SectionTwo',
    
}

</script>

<template>
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
</template>

<style lang="scss" scoped>
@use '/src/styles/main.scss' as *;

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
