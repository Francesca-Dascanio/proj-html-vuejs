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
    background-image: url('/src/assets/avadabarbers-about-introbackground.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    
        .container-sm {

            padding: 2rem 0 4rem 0;
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
