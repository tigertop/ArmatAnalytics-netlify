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

:root {
    --cornflowerblue-color: #72AFF7;
    --midnightblue-color: #013164;
    --darkturquoise-color: #00b6e0;
    --darkslategray-color: #25546d;
    --mediumturquoise-color: #37bfef;
    --ghostwhite-color: #f9fbfc;
    --lightsteelblue-color: #c2b6e5;
    --white-color: #ffffff;
    --navy-color: #25546D;
    --darkerblue-color: #263E52;
    --justsky-color: #f5f8fb;
}

.container{
    max-width: 1440px;
}

@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&family=Source+Sans+Pro:wght@200;300;400;600;700;900&display=swap');
</style>