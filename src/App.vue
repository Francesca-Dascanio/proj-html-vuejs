<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';

export default {
    name: 'App',
    components: {
        AppHeader,
        AppMain,
        AppFooter
    },
    data () {
        return {
            headerMenu: [
                'Home',
                'About Us',
                'Services',
                'Shop',
                'Our Team',
                'Blog',
                'Contact Us'
            ],
            footerContacts: [
                {
                    name: 'Avada Barbers',
                    address: '123 New York Street',
                    city: 'New Yprk City',
                    email: 'info@yourwebsite.com',
                    phone: '+1 (555) 555-1212'
                }
            ]
        }
    }
}

</script>

<template>

    <AppHeader />
    <AppMain />
    <AppFooter />
  
</template>

<style lang="scss">
@import './styles/main.scss';

</style>
