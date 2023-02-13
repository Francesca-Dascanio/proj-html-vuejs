<script>

export default {
    name: 'SectionOne',
    
}

</script>

<template>
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
</template>

<style lang="scss" scoped>
@use '/src/styles/main.scss' as *;

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


</style>
