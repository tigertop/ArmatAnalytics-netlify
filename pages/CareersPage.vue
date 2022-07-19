<template>
    <div>
        <!-- Start wrap -->
        <section v-for="(key, index) in keyTosuccess" :key="index" class="careers-wrap"  :style="{backgroundImage: 'url(' + key.image + ')'}">
            <b-container class="pt-5">
                <b-row class="pt-4">
                    <b-col class="pt-lg-4 text-center">
                        <h2 class="wrap-title pt-lg-5">{{ key.title }}</h2>
                        <p class="pt-3 wrap-description">{{ key.description }}</p>
                    </b-col>
                </b-row>
            </b-container>
        </section>
        <!-- End wrap -->
        <!-- Start Why-join -->
        <div id="join-boxes" >
            <div id="why-join" class="text-center pt-5 bg-white">
                <h1 class="py-5 title">Why join Armat Analytics?</h1>
            </div>
            <b-container class="my-5 p-5">
                <div class="py-5">
                    <b-row class="row g-5">
                        <b-col class="mb-4" v-for="(why, index) in whyJoin" :key="index" md="6" lg="6" sm="12" >
                            <div class="shadow-w round-w bg-white h-100 p-2">
                                <b-row class="pt-4">
                                    <b-col md="2" class="text-center">
                                        <img class="align-item-center" :src="why.icon" alt="">
                                    </b-col>
                                    <b-col md="6" class="pt-2">
                                        <div class="text-lg-left text-md-left text-center">
                                        <h6 class="pb-2 box-t">{{ why.title }}</h6>
                                        </div>
                                    </b-col>
                                </b-row>
                                <b-row>
                                    <b-col md="2"></b-col>
                                    <b-col md="9">
                                        <p class="pb-3 box-d">{{ why.description }}</p>
                                    </b-col>
                                </b-row>
                            </div>
                        </b-col>
                    </b-row>
                </div>
            </b-container>
        </div>
     <!-- end Why-join -->
     <!-- Start The Root -->
        <section class="root pt-5" id="root">
            <b-container class="bv-example-row">
                <b-row align-h="center">
                    <b-col cols lg="5" md="5" sm="12" class="text-lg-left">
                        <div class="pt-5">
                            <p class="root-p">Armat Analytics’s social mission is to educate new generations of programmers who will support the life saving industry of medication and drug development. </p>
                        </div>
                    </b-col>
                    <b-col cols lg="5" md="5" sm="12" class="text-lg-right">
                        <img class="img-fluid" src="/images/hoodie-guy-right.png" alt="">
                    </b-col>
                </b-row>
                <b-row align-h="center" class="ml-lg-5 pt-lg-5 pt-sm-5">
                    <b-col cols lg="5" md="5" sm="12" class="text-lg-left">
                        <div class="m-lg-3">
                           <img class="img-fluid me-lg-5" src="/images/hoodie-guy-left.png" alt="">
                        </div>
                    </b-col>
                    <b-col cols lg="5" md="5" sm="12" class="text-lg-left">
                        <div class="pt-lg-5 ml-lg-5">
                            <p class="root-p">Our training program  “The ROOT ”  is designed to teach you the fundamentals of statistical programming and clinical reporting! </p>
                        </div>
                        <div class="pt-lg-3 ml-lg-5">
                            <h2 class="root-h2">Your only investment is your <span class="h2color">time</span> and <span class="h2color">dedication</span>.</h2>
                        </div>
                    </b-col>
                </b-row>
                <b-row class="pt-5">
                    <div class="col-2"></div>
                    <div class="col-8 dashed-container pt-5">
                        <div class="text-center pb-1">
                            <h5 class="pb-4">The Root will teach you:</h5>
                        </div>
                        <div class="row">
                            <div class="col-md-6 col-xs-12 d-flex justify-content-center">
                                <ul>
                                    <li>Fundamentals of Programming</li>
                                    <li>SAS base programming</li>
                                    <li>SQL</li>
                                    <li>Fundamentals of statistics</li>
                                </ul>
                            </div>
                            <div class="col-md-6 col-xs-12 ul2 pb-5 d-flex justify-content-center">
                                <ul>
                                    <li>Working with Statistical Procedures</li>
                                    <li>SAS Macro language</li>
                                    <li>Data visualization with SAS</li>
                                    <li>Clinical Data Standardization and Reporting</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </b-row>
            </b-container>
            <div class=" text-center pt-5">
            <small>It is a unique opportunity to take your first steps in the biotechnology industry and become a part of change that matters.</small>
            </div>
            <div class=" text-center pb-5">
            <small><b>Join the program, </b> show your best and be among the selected students who will join the Armat team! </small>
            </div>
            <div class=" text-center py-4">
            <button type="button" class="btn btn-primary btn-lg text-capitalize">Submit application</button>
            </div>
      </section>
     <!-- End The Root -->
    <!-- accordion -->
        <section class="section-background pb-5">
            <b-row class="text-center py-5">
                <b-col class="col">
                <h1 class="title">Our vacancies</h1>
                </b-col>
             </b-row>
            <b-container class="accordion-container" id="accordion">
                <div v-for="(vacancy, index) in ourVacancies" :key="index" class="accordion" role="tablist">
                    <b-card no-body class="accordion-item">
                        <b-card-header class="border-0 py-4 bg-transparent" role="tab">
                            <div class="left-border"></div>
                            <b-button class="accordion-button accordion-button-noborder d-flex justify-content-between"
                            block v-b-toggle.accordion-1 variant="transparent">
                                <h6 class="mb-lg-0 text-left sas-font">{{ vacancy.title }}</h6>
                                <b-img class="plus-icon" src="images/icons8-plus-50.png" width="30"></b-img>
                            </b-button>
                        </b-card-header>
                        <b-collapse id="accordion-1" accordion="my-accordion" role="tabpanel">
                            <b-card-body class="accordion-body">
                                <b-card-text v-html="$md.render(vacancy.description)"></b-card-text>
                                <div class="text-lg-right my-3">
                                    <b-button type="button" class="btn btn-primary btn-lg border-0 text-capitalize">Submit application</b-button>
                                </div>
                            </b-card-body>
                        </b-collapse>
                    </b-card>
                </div>
            </b-container>
        </section>
      <!-- /accordion -->
    </div>
</template>

<script>
import _ from 'lodash'
export default {
    name: 'CareersPage',
    async asyncData({ $content }) {
        let keyTosuccess = await $content('keytosuccess').fetch();
        let whyJoinContents = await $content('whyjoin').fetch();
        let whyJoin = _.orderBy(whyJoinContents, 'sortkey');
        let ourVacancies = await $content('ourvacancies').fetch();

        return {
            keyTosuccess,
            whyJoin,
            ourVacancies
        }
    }
}
</script>

<style>


body {
    font-family:'Source Sans Pro', sans-serif;
}

button {
    display: block;
    border: none;
}

.row h6 {
    font-family: 'Poppins';
    font-size: 17px;
    font-weight: bold;
}

.careers-wrap {
    background-repeat: no-repeat;
    background-size: cover;
    height: 60vh;
}

.wrap-title {
    font-size: 2.375em;
    letter-spacing: .08rem;
    font-weight: 400;
    line-height: 1.2;
    color: white;
}

.wrap-description{
    font-size: 1.625em;
    font-weight: 300;
    letter-spacing: .08rem;
    color: white;
}

.shadow-w {
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 28px;
}
.round-w {
    border-radius: 1rem;
}

.box-d {
    font-size: 1.063em;
    font-family: 'Open Sans', sans-serif;
    font-weight: 400;
    color: #67748E;
}

.box-t {
    font-family: 'Open Sans', sans-serif;
    font-size: 1.375em;
    color: #252F40;
    font-weight: 600;
}

#join-boxes {
    background-color: #F9FBFC;
}



/* accordion */

.bg-transparent {
    box-shadow: none!important;
}
.accordion-container {
    max-width: 1100px;
}
.section-background {
    background-color: #F9FBFC;
}

.sas-font{
    font-weight: 600;
    font-size: 1.250em;
    color: #263E52;
}

.card-text {
    color: #263E52;
    opacity: .95;
    font-size: 1.063em;
}
#accordion .accordion-item {
    border: .12em solid #81C3FD;
    border-radius: 5px;

}

.card-header{
    position: relative;
    box-shadow: none!important;
}

.accordion-button-noborder:not(.collapsed){
    box-shadow: none!important;
    background-color: #F9FBFC!important;
}
.accordion-button-noborder.collapsed{
    background-color: #F9FBFC!important;
    box-shadow: none!important;
}

.card-header .left-border {
    background-color: #81C3FD;
    width: 5px;
    height: 25px;
    position: absolute;
    left: -1px;
    top: calc(50% - 10px);
    z-index: 2;
}


.plus-icon{
    transition: .3s;
}

.accordion-button:not(.collapsed) .plus-icon{
    transform: rotate(-137deg)!important;
    transition: .3s;
}

/* .accordion-button:not(.collapsed):after {
    transform: rotate(-137deg)!important;
}

.accordion-button:after {
    background-image: url(static/images/icons8-plus-50.png)!important;
} */

#accordion .btn-primary {
    background-color:var(--cornflowerblue-color);
    font-family: 'Source Sans Pro';
    font-size: 16px;
}

#accordion {
    background-color: #F9FBFC;
}

#accordion .accordion-item {
    background-color: transparent;
}

/* #accordion .accordion-header{
    box-shadow:#F9FBFC!important;
} */
/* /accordion */
/*  root */
.root-p {
    font-family: 'Source Sans Pro';
    font-size: 24px;
    color: var(--darkerblue-color);
}

.root-h2 {
    font-family: 'Source Sans Pro';
    font-weight: 600;
    color: var(--darkerblue-color);
}
.root h5 {
    font-family: 'Source Sans Pro';
    font-weight: 600;
    color: var(--darkerblue-color);
    font-size: 20px;
}

.root-h2 .h2color {
    font-family: 'Source Sans Pro';
    font-weight: 600;
    color: var(--cornflowerblue-color);
    font-size: 32px;
}

.root {
    background-image: url('/images/Tracé\ 2.svg');
    background-size: 100vh 100%;
    position: relative;
    background-repeat: no-repeat;
    z-index: 10;
}

/*  root */
</style>