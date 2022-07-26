<template>
  <div>
    <!-- Start Presentation -->
    <section class="py-13 bg-cover img-responsive d-block">
      <b-container class="py-6 py-md-5 mb text-white z-index-20">
        <b-row class="mt-3 py-4 px-2">
          <b-col lg="12" class="mt-5">
            <div class="text-lg-left text-center">
              <h1 class="title-h1 font-weight-bold py-md-5 mt-5 text-shadow d-block">
                See the change with Armat. <br />
                <vue-typer :text='["Delivering Quality", "Armat Diligence", "Armat Innovation"]' initial-action='typing'></vue-typer>
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
          <h1 class="about title">{{ data.title }}</h1>
          <p class="lead description">
            {{ data.body.children[0].children[0].value }}
          </p>
        </b-col>
        <b-col lg="6" md="6" sm="12">
          <div class="text-lg-right">
            <b-img class="m-view-about" :src="data.image" fluid alt="Responsive image" ></b-img>
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
            <b-img class="m-view-mission" :src="data.image" fluid alt="Responsive image"></b-img>
          </div>
        </b-col>
        <b-col lg="5" order-lg="2" md="5" order-md="2" sm="12" order="1">
          <h1 class="mission title">{{ data.title }}</h1>
          <p class="lead description">
            {{ data.body.children[0].children[0].value }}
          </p>
        </b-col>
      </b-row>
    </b-container>
    <!-- End Our mission-->
    <!-- Start Our Services -->
    <section id="our-services" class="p-lg-5">
      <b-container class="pt-5">
        <b-row v-for="(data, index) in ourServices" :key="index" class="pt-5 d-flex">
          <div
            class="col-lg-12 ms-lg-5r text-center p-5"
            style="background-color: #f5f8fb; border-radius: 1rem"
          >
            <h1 class="fw-bold title">{{ data.title }}</h1>
            <p class="b-5 description">
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
          <h1 class="title">Reporting</h1>
          <p class="description">We provide both full and partial support for Phase 1-4 study reporting.</p>
        </b-col>
      </b-row>
      <b-row class="g-5 justify-content-around align-self-stretch">
        <b-col lg="4" md="6" sm="12" v-for="(report, index) in reporting" :key="index" class="text-center align-items-stretch mb-4">
          <div class="p-5 shadow-r radius-1 h-100">
            <div class="my-3">
              <img class="align-item-center" :src="report.icon" alt="" />
            </div>
            <h6 class="report-h6">{{ report.title }}</h6>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <!-- End Reporting -->
    <!-- Start Data Managment -->
    <b-container class="p-5">
      <b-row id="data" class="text-center my-5">
        <b-col cols="12">
          <h1 class="title">Data Management services</h1>
          <p class="description">We also support you in data management procedures.</p>
        </b-col>
      </b-row>
      <b-row class="justify-content-around d-flex justify-content-between">
        <b-col col lg="4" md="6" sm="12" v-for="(data, index) in dataManagement" :key="index" class="text-center align-items-stretch">
          <b-jumbotron class="dtmgmt rounded-hover bg-light m-lg-5 p-5 h-75" :style="{'--hovercolor':data.color}">
            <div class="icon-box align-items-center">
              <div class="icon my-lg-3 my-md-3">
                <div class="icon-bg-circle" :style="{backgroundColor:data.color}">
                  <img class="icon-img-center" :src="data.icon" alt="" />
                </div>
              </div>
              <h5 class="d-description">{{ data.title }}</h5>
            </div>
          </b-jumbotron>
        </b-col>
      </b-row>
    </b-container>
    <!-- End Data Managment -->
    <!-- Start Therapeutic Areas -->
    <section class="pt-3 bg-light-grey">
      <b-container v-for="(area, index) in therapeuticAreas" :key="index"  class="bv-example-row bv-example-row-flex-cols">
        <b-row id="therapeutic" class="text-center my-5">
          <b-col cols="12">
            <h1 class="title">{{ area.title }}</h1>
            <p class="description">{{ area.description }}</p>
          </b-col>
        </b-row>
        <b-row >
          <b-col align-self="center" cols="12" class="text-center my-5">
            <b-img :src="area.image" fluid alt="Fluid image"></b-img>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <!-- End Therapeutic Areas -->
    <!-- Start Join Aramt -->
    <div id="learn" v-for="(join, index) in joinArmat" :key="index">
      <b-row id="join-us" class="text-center p-5 mt-5">
        <b-col>
          <h1 class="title">{{ join.title }}</h1>
          <p class="description">{{ join.description }}</p>
        </b-col>
      </b-row>
      <section class="img-responsive" :style="{backgroundImage: 'url(' + join.image + ')'}">
        <b-container fluid="sm" class="bv-row bv-row-flex-cols pt-5">
          <b-row class="text-center pt-5" >
            <b-col  align-self="center" cols="12" class="text">
              <div>
                <span class="pt-lg-5 lrn-description">{{ join.body.children[0].children[0].value }}</span>
              <b-col class="pt-5">
                <a href="/careers" variant="primary" type="button" class="btn btn-lg btn-primary  border-0" role="button">Learn More</a>
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
    let therapeuticAreas = await $content('therapeuticareas').fetch();
    let joinArmat = await $content('joinarmat').fetch();

    return {
      aboutUs,
      ourMission,
      ourServices,
      reporting,
      dataManagement,
      therapeuticAreas,
      joinArmat
    }
  }
}
</script>

<style>
.vue-typer .custom.char.typed {
  color: #fff;
}
.vue-typer .custom.char.selected {
  color: #fff;
  background-color: transparent;
}
.vue-typer .custom.caret {
  width: 5px;
  background-color: #00b5df;
}

.bg-cover {
  height: 81vh;
  background-image: url(/images/Desktop1.png);
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
}

 .bg-light-grey{
  background-color: #F9FBFC;
 }

.title {
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 2.8em;
  color: #263e52;
  font-weight: 600;
}

.description {
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 1.25em;
  color: #263e52;
  letter-spacing: 0.02rem;
  font-weight: 400;
}

.area-description {
  font-size: 1em;
  font-weight: 600;

}

.title-h1 {
  font-size: 4.375em;
}

.report-h6 {
  font-family:'Poppins', sans serif;
  font-size: 1.125em;
  font-weight: 500!important;
}

#reporting .shadow-r {
  box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 28px;
}

.radius-1 {
  border-radius: 1.8rem;
}

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

.rounded-hover {
  border-radius: 0.75rem;
  border: none;
}

.d-description {
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 1.125em;
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

.lrn-description {
  font-family: 'Source Sans Pro', sans-serif;
  font-weight: 300;
  font-size: 1.25em;
  color: white
}

#learn .btn {
  background-color: #37BFEF;
  font-size: 1em;
}

#learn .img-responsive {
  background-repeat: no-repeat;
  background-size: cover;
  height: 55vh;
}

@media only screen and (min-width: 800px) {
  .m-view-about {
    width: 85%;
  }
}

@media only screen and (min-width: 800px) {
 .m-view-mission{
    width: 75%;
  }
}



</style>