<template>
    <div class="site">
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

body,html {
  overflow-x:hidden;
  scroll-behavior: smooth;
}

.site {
    overflow-x: hidden;
    width: 100%;
}

.container{
    max-width: 1440px;
}

.products .dropdown-toggle::after {
  border: none !important;
}
</style>