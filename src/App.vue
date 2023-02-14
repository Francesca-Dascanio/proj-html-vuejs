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
            clicked: false,
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
                'Avada Barbers',
                '123 New York Street',
                'New York City',
                'info@yourwebsite.com',
                '+1 (555) 555-1212'
            ]
        }
    }
}

</script>

<template>

    <div class="general-container" 
    :class="{
        '': clicked == false,
        'not-visible': clicked == true
    }">
        <AppHeader @getClick="clicked = true" />
        <AppMain />
        <AppFooter :footerContacts="footerContacts"/>
    </div>

    <div class="general-menu" 
    :class="{
        'not-visible': clicked == false,
        '': clicked == true
    }">
        <div class="exit text-right" @click="clicked = false">
            <font-awesome-icon icon="fa-solid fa-xmark" />
        </div>
        <div class="menu-container flex justify-center align-items">
            <ul > 
                <li v-for="info in headerMenu">
                    <a href="#">
                        {{ info }}
                    </a>
                </li>
            </ul>
        </div>
    </div>
    
</template>

<style lang="scss">
@import './styles/main.scss';

.general-menu {
    background-color: $fourth-color;
    color: $fifth-color;
    width: 100%;
    height: 100vh;

        .exit {
            padding: 1rem;
        }

       .menu-container {

            height: 100%;

            ul {
                list-style: none;

                li {
                    text-align: center;
                    padding: 0.5rem;

                    a {
                        text-decoration: none;
                        color: $fifth-color;
                        padding: 0.5rem;

                        &:hover {
                            color: $primary-color;
                        }
                    }
                }
            }
       }

}

</style>
