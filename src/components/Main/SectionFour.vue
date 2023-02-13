<script>

export default {
    name: 'SectionFour',
    
}

</script>

<template>
    <section id="section-4">
        <div class="container-lg">
            <div class="container-sm">
                <div class="section-title text-center py-md">
                    <h5>
                    Lorem ipsum dolor sit.
                    </h5>
                    <h2>
                        SECTION 4 TITLE
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
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '/src/styles/main.scss' as *;


#section-4 {
    .container-lg {
    background-color: lightblue;
        .container-sm {
            background-color: lightcoral;

            .section-contents {
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
