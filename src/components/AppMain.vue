<script>
import SectionOne from './Main/SectionOne.vue';
import SectionTwo from './Main/SectionTwo.vue';
import SectionThree from './Main/SectionThree.vue';
import SectionFour from './Main/SectionFour.vue';
import SectionFive from './Main/SectionFive.vue';

export default {
    name: 'AppMain',
    components: {
        SectionOne,
        SectionTwo,
        SectionThree,
        SectionFour,
        SectionFive
    },
    data () {
        return {
            // Qui andranno data delle section-cards
        }
    }
}

</script>

<template>

    <main>

        <SectionOne />

        <SectionTwo />

        <SectionThree />

        <SectionFour />

        <SectionFive />
      
    </main>

</template>

<style lang="scss" scoped>
 

</style>
