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
    <!-- accordion -->
      <b-container fluid class="cmy-5 py-5" id="accordion">
          <b-row class="row text-center">
            <b-col>
              <h1>Our vacancies</h1>
            </b-col>
          </b-row>
            <b-row class="justify-content-center">
            <b-col lg="6" md="6" sm="12">
                <div class="accordion accordion-flush pt-5 py-5" id="accordionFlushExample">
                <div class="accordion-item py-2">
                    <h2 class="accordion-header" id="flush-headingOne">
                    <div class="left-border"></div>
                    <button class="accordion-button accordion-button-noborder collapsed" type="button" data-bs-toggle="collapse" data-bs-target="#flush-collapseOne" aria-expanded="false" aria-controls="flush-collapseOne">
                        <h6>SAS Programmer</h6>
                    </button>
                    </h2>
                    <div id="flush-collapseOne" class="accordion-collapse collapse" aria-labelledby="flush-headingOne" data-bs-parent="#accordionFlushExample">
                    <div class="accordion-body">
                        <p>Job Description</p>
                        <p>Responsible for implementing recurring solution integrations at our clients’ companies. Will work closely with Product Development team for knowledge transfer and documentation on new integrations </p>
                        <div class="text-lg-end text-xs-center py-3">
                        <button type="button" class="btn btn-primary btn-lg text-capitalize">Submit application</button>
                        </div>
                    </div>
                    </div>
                </div>
                </div>
            </b-col>
            </b-row>
        </b-container>
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

    return {
        keyTosuccess,
        whyJoin
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
#accordion .accordion-item {
    border: .12em solid #81C3FD;
    border-radius: 5px;

}

.accordion-header{
    position: relative;
}

.accordion-header button{
    font-weight: bold!important;
    font-family: 'Source Sans Pro';
}

.accordion-button-noborder:not(.collapsed){
    box-shadow: none!important;
    background-color: #F9FBFC!important;
}
.accordion-button-noborder.collapsed{
    background-color: #F9FBFC!important;
}

.accordion-header .left-border {
    background-color: #81C3FD;
    width: 4px;
    height: 20px;
    position: absolute;
    left: -1px;
    top: calc(50% - 10px);
    z-index: 9;
}

.accordion-button:not(.collapsed):after {
    transform: rotate(-137deg)!important;
}

.accordion-button:after {
    background-image: url(static/images/icons8-plus-50.png)!important;
}

.accortion-body p {
    font-family: 'Source Sans Pro';
    color: var(--darkerblue-color);
}

#accordion .btn-primary {
    background-color:var(--cornflowerblue-color);
    font-family: 'Source Sans Pro';
    font-size: 16px;
}

#accordion {
    background-color: #F9FBFC;
}
#accordion h1 {
    font-family: 'Source Sans Pro';
    font-size: 44px;
    font-weight: 600;
    color: var(--darkerblue-color)
}

#accordion .accordion-item {
    background-color: transparent;
}


#accordion .accordion-header{
    box-shadow:#F9FBFC!important;
}

/* /accordion */
</style>