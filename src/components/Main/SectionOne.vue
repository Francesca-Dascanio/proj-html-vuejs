<script>

export default {
    name: 'SectionOne',
    
}

</script>

<template>
    <section id="section-1">
        <div class="container-lg bg-img">
            <div class="container-sm">
                <div class="section-title text-center py-md">
                    <h5>
                        AWARD WINNING
                    </h5>
                    <h2>
                        Pro Barbers
                    </h2>
                </div>

                <div class="section-contents flex align-items py-md">
                    <button>
                        MEET YOUR NEW BARBER
                    </button>
                </div>
            </div>
            <div class="container-lg triangle">
                <svg class="fusion-big-triangle-candy" xmlns="http://www.w3.org/2000/svg" version="1.1" width="100%" height="60px" viewBox="0 0 100 100" preserveAspectRatio="none" style="fill:#ffffff;padding:0;"><path d="M0 100 L50 2 L100 100 Z"></path></svg>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
@use '/src/styles/main.scss' as *;


#section-1 {
    .bg-img {
        @include bg-image ('/src/assets/avadabarbers-about-introbackground.jpg', initial);
        .container-sm {

            padding: 3rem 0;
            .section-contents {
                flex-direction: column;

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
