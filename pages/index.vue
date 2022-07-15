<template>
  <div>
    <!-- Start Presentation -->
    <section class="py-13 bg-cover img-responsive d-block">
      <b-container class="py-6 py-md-5 mb text-white z-index-20">
        <b-row class="mt-3 py-4 px-2">
          <b-col lg="12" class="mt-5">
            <div class="text-left">
              <h1 class="h1 font-weight-bold py-md-5 mt-5 text-shadow">
                See the change with Armat. <br />
                Delivering Quality
              </h1>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <!-- End Presentation -->

    <!-- Start About us -->
    <b-container id="about" class="bv-example-row pt-5">
      <b-row v-for="(data, index) in aboutUs" :key="index" align-h="between pt-5">
        <b-col lg="6" md="6" sm="12">
          <h1 class="about">{{ data.title }}</h1>
          <p class="lead">
            {{ data.body.children[0].children[0].value }}
          </p>
        </b-col>
        <b-col lg="6" md="6" sm="12">
          <div class="text-lg-right">
            <b-img :src="data.image" fluid alt="Responsive image" style="width: 85%"></b-img>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <!-- End About us -->

    <!-- Start Our mission-->
    <b-container id="our-mission" class="container bv-example-row pt-5">
      <b-row v-for="(data, index) in ourMission" :key="index" align-h="between pt-5">
        <b-col lg="7" order-lg="1" md="7" order-md="1" sm="12" order="2">
          <div class="text-left">
            <b-img :src="data.image" fluid alt="Responsive image" style="width: 75%"></b-img>
          </div>
        </b-col>
        <b-col lg="5" order-lg="2" md="5" order-md="2" sm="12" order="1">
          <h1 class="mission">{{ data.title }}</h1>
          <p class="lead">
            {{ data.body.children[0].children[0].value }}
          </p>
        </b-col>
      </b-row>
    </b-container>
    <!-- End Our mission-->

    <!-- Start Our Services -->
    <section id="our-services" class="p-5">
      <b-container class="pt-5">
        <b-row v-for="(data, index) in ourServices" :key="index" class="pt-5 d-flex">
          <div
            data-aos="fade-up"
            data-aos-duration="1350"
            class="col-lg-12 ms-lg-5r text-center p-5"
            style="background-color: #f5f8fb; border-radius: 1rem"
          >
            <h1 class="fw-bold">{{ data.title }}</h1>
            <p class="b-5">
              {{ data.body.children[0].children[0].value }}
            </p>
          </div>
        </b-row>
      </b-container>
    </section>
    <!-- end Our Services  -->

       <!-- Start Reporting -->
    <b-container id="reporting" class="p-2">
      <b-row class="text-center my-5">
        <b-col cols="12">
          <h1>Reporting</h1>
          <p>We provide both full and partial support for Phase 1-4 study reporting.</p>
        </b-col>
      </b-row>
      <b-row class="row-cols-2 row-cols-lg-3 g-5 justify-content-around align-self-stretch">
        <b-col v-for="(report, index) in reporting" :key="index" class="text-center align-items-stretch mb-4">
          <div class="p-5 shadow-r rounded-4 radius-1 h-100">
            <b-icon class="my-3">
              <img class="align-item-center" :src="report.icon" alt="" />
            </b-icon>
            <h6>{{ report.title }}</h6>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <!-- End Reporting -->

    <!-- Start Data Managment -->
    <b-container class="p-5">
      <b-row id="data" class="text-center my-5">
        <b-col cols="12">
          <h1>Data Management services</h1>
          <p>We also support you in data management procedures.</p>
        </b-col>
      </b-row>
      <b-row class="justify-content-around d-flex justify-content-between">
        <b-col v-for="(data, index) in dataManagement" :key="index" lg="4" md="6" class="text-center align-items-stretch">
          <b-jumbotron class="dtmgmt rounded-hover bg-light m-5 p-5 h-75" :style="{'--hovercolor':data.color}">
            <div class="icon-box align-items-center">
              <div class="icon my-3">
                <div class="icon-bg-circle" :style="{backgroundColor:data.color}">
                  <img class="icon-img-center" :src="data.icon" alt="" />
                </div>
              </div>
              <h5>{{ data.title }}</h5>
            </div>
          </b-jumbotron>
        </b-col>
      </b-row>
    </b-container>
    <!-- End Data Managment -->

    <!-- Start Terapeutic Areas -->
    <!-- <section class="areas pt-3">
      <b-container class="bv-example-row bv-example-row-flex-cols">
      <b-row id="therapeutic" class="text-center my-5">
        <b-col cols="12">
          <h1>Therapeutic Areas</h1>
          <p>We also support you in data management procedures. </p>
        </b-col>
      </b-row>
      <b-row >
        <b-col align-self="center" cols="12" class="text-right my-5" style="border-image: url('images/therapeutic.png'); border:3px">
          <img src="images/ellipse 15.png" alt="">
        </b-col>
      </b-row>
    </b-container>
    </section> -->


    <div class="bg-image img-fluid bg-therapeutic" >
      <img class="bgtop1" src="images/medical-records.png" alt="">
      <img class="bg2" src="images/oncology.png" alt="">
      <img class="bg3" src="images/virus.png" alt="">
      <img class="bg4" src="images/brain.png" alt="">
      <img class="bg5" src="images/dermatology.png" alt="">
      <img class="bg6" src="images/immunity.png" alt="">
    </div>



    <!-- <div class="container-fluid bg-light">
    <div id="data" class="row text-center my-5 p-5">
      <h1>Therapeutic Areas</h1>
      <p>We also support you in data management procedures. </p>
      <h1 class="display-1 p-5">***************</h1>
      <h1 class="display-1 p-5">COMING SOON</h1>
      <h1 class="display-1 p-5">***************</h1>
    </div>
  </div> -->

    <!-- End Terapeutic Areas -->

    <!-- Start Join Aramt -->
    <div id="learn" v-for="(join, index) in joinArmat" :key="index">
      <b-row id="join-us" class="text-center p-5">
        <b-col>
          <h1>{{ join.title }}</h1>
          <p>{{ join.description }}</p>
        </b-col>
      </b-row>
      <section class="img-responsive" :style="{backgroundImage: 'url(' + join.image + ')'}">
        <b-container fluid="sm" class="bv-row bv-row-flex-cols pt-5">
          <b-row class="text-center pt-5" >
            <b-col  align-self="center" cols="12" class="text">
              <div>
                <span class="pt-lg-5">{{ join.body.children[0].children[0].value }}</span>
              <b-col class="pt-lg-5">
                <b-button variant="primary" size="lg" type="button" class="btn">Learn More</b-button>
              </b-col>
              </div>
            </b-col>
          </b-row>
        </b-container>
      </section>
    </div>
    <!-- End Join Aramt -->
  </div>
</template>

<script>
import _ from 'lodash'
export default {
  name: 'IndexPage',
  async asyncData({ $content, error }) {
    let reporting
    try {
      let reportingContents = await $content('reporting').fetch()
      reporting = _.orderBy(reportingContents, 'sortkey')
    } catch (e) {
      error({ message: 'Reporting not found' })
    }
    let dataManagement
    try {
      let dataManagementContents = await $content('dataManagement').fetch()
      dataManagement = _.orderBy(dataManagementContents, 'sortkey')
    } catch (e) {
      error({ message: 'Data Management not found' })
    }
    let aboutUs = await $content('aboutus').fetch();
    let ourMission = await $content('ourmission').fetch();
    let ourServices = await $content('ourservices').fetch();
    let joinArmat = await $content('joinarmat').fetch();

    return {
      aboutUs,
      ourMission,
      ourServices,
      reporting,
      dataManagement,
      joinArmat
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&family=Source+Sans+Pro:wght@200;300;400;600;700;900&display=swap');

.bg-cover {
  height: 81vh;
  background-image: url(/images/Desktop1.png);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}

h1 {
  font-family: 'Source Sans Pro';
}

p {
  font-family: 'Source Sans Pro';
}

h1.h1 {
  font-size: 70px;
}

#about h1 {
  font-size: 45px;
  color: #263e52;
  font-weight: 600;
}

#about p {
  font-size: 20px;
  color: #263e52;
  letter-spacing: 0.02rem;
  font-weight: 400;
}

#our-mission h1 {
  font-size: 45px;
  color: #263e52;
  font-weight: 600;
}

#our-mission p {
  font-size: 20px;
  color: #263e52;
  letter-spacing: 0.02rem;
  font-weight: 400;
}

#our-services h1 {
  font-size: 45px;
  font-weight: 700;
  color: #263e52;
}

#our-services p {
  font-size: 20px;
  font-weight: 400;
  color: #263e52;
}

#reporting h1 {
  font-size: 45px;
  font-weight: 600;
  color: #263e52;
}

#reporting p {
  font-size: 20px;
  letter-spacing: 0.02rem;
  font-weight: 400;
}

#reporting .shadow-r {
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 28px;
}

#data h1 {
  font-size: 45px;
  font-weight: 600;
  color: #263e52;
}

#data p {
  font-size: 20px;
  letter-spacing: 0.02rem;
  font-weight: 400;
}

.radius-1 {
  border-radius: 1.8rem;
}

/* start Data icon-box */
.icon-bg-circle {
  display: inline-block;
  position: relative;
  width: 72px;
  height: 72px;
  border-radius: 50%;
  vertical-align: middle;
}

.icon-img-center {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
/* end Data icon-box */
/* border hover start */

.rounded-hover {
  border-radius: 0.75rem;
  border: none;
}

.rounded-hover h5 {
  font-family: 'Source Sans Pro';
  font-size: 18px;
  font-weight: 500;
  color: #263E52;
}

.dtmgmt.rounded-hover:hover {
  -webkit-box-shadow: 0px 0px 0px 3px var(--hovercolor);
  -moz-box-shadow: 0px 0px 0px 3px var(--hovercolor);
  box-shadow: 0px 0px 0px 3px var(--hovercolor);
  transition: 0.333s;
  cursor: pointer;
}
/* border hover end */

#learn span {
  font-family: 'Source Sans Pro';
  font-weight: 300;
  font-size: 20px;
  color: white
}

#join-us h1 {
  font-size: 45px;
  font-weight: 600;
  color: #263e52;
}

#join-us p {
  font-size: 20px;
  font-weight: 400;
  color: #263e52;
}

#learn .btn {
  background-color: #37BFEF;
  font-size: 16px;
}

#learn .img-responsive {
  background-repeat: no-repeat;
  background-size: cover;
  height: 55vh;
}

#therapeutic h1{
  font-size: 45px;
  font-weight: 600;
  color: #263e52;
}

#therapeutic p{
  font-size: 20px;
  font-weight: 400;
  color: #263e52;
}
.areas {
  background-color: #F9FBFC;
}

@media only screen and (min-width: 1425px) {
  .bgtop1{
    position: absolute;
    top: 36%;
    left: 50.2%;
    z-index: 2;

  }
  .bg2 {
  position: absolute;
  top: 47.5%;
  left: 61.8%;
  z-index: 2;

}

.bg3 {
  position: absolute;
  top: 72.7%;
  left: 63%;
  z-index: 2;
}

.bg4 {
  position: absolute;
  top: 86%;
  left: 50%;
  z-index: 2;
}

.bg5 {
  position: absolute;
  top: 72.7%;
  left: 37%;
  z-index: 2;
}

.bg6 {
  position: absolute;
  top: 47.5%;
  left: 38%;
  z-index: 2;
}
}

.bg-therapeutic {
  background-image: url('static/images/empty.png');
  background-size: cover;
  width: auto;
  height: 110vh;
  position: relative;
  background-repeat: no-repeat;
  z-index: 1;
}

</style>