<template>
    <div>
        <AppHeader />
        <Nuxt />
        <ContactUs />
        <AppFooter />
    </div>
</template>

<script>
import AppHeader from '~/components/global/AppHeader.vue';
import ContactUs from '~/components/global/ContactUs.vue';
import AppFooter from '~/components/global/AppFooter.vue';

export default {
    name: 'default',
    components: {
        AppHeader,
        ContactUs,
        AppFooter
    }
}
</script>

<style>
body, html {
   margin: 0;
   padding: 0;
}

body{
   overflow-x: hidden;
}

.container{
    max-width: 1440px;
}

</style>