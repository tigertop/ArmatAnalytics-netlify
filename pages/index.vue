<template>
  <div>
    <!-- Start Presentation -->
    <section class="py-13 bg-image bg-cover img-responsive d-block">
      <div class="container py-6 py-md-5 mb text-white z-index-20">
        <div class="row mt-3 py-4 px-2">
          <div class="col-lg-12 mt-5">
            <div class="text-left">
              <h1 class="h1 font-weight-bold py-md-5 mt-5 text-shadow">
                See the change with Armat. <br />
                Delivering Quality
              </h1>
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- End Presentation -->

    <!-- Start About us -->
    <b-container id="about" class="bv-example-row pt-5">
      <b-row align-h="between pt-5">
        <b-col lg="6" md="6" sm="12">
          <h1 class="about">About us</h1>
          <p class="lead">
            Armat Analytics is a Functional Service Provider specialized in statistical programming, data management and
            clinical database design. Our flexible work model allows us to easily adapt to any environment. We smoothly
            integrate into the processes, as we can work both with already established structures and implement our own
            management and operational <br />
            procedures.
          </p>
        </b-col>
        <b-col lg="6" md="6" sm="12">
          <div class="text-lg-right">
            <b-img src="/images/about.png" fluid alt="Responsive image" style="width: 85%"></b-img>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <!-- End About us -->

    <!-- Start Our mission-->
    <b-container id="our-mission" class="container bv-example-row pt-5">
      <b-row align-h="between pt-5">
        <b-col lg="7" order-lg="1" md="7" order-md="1" sm="12" order="2">
          <div class="text-left">
            <b-img src="/images/mission.png" fluid alt="Responsive image" style="width: 75%"></b-img>
          </div>
        </b-col>
        <b-col lg="5" order-lg="2" md="5" order-md="2" sm="12" order="1">
          <h1 class="mission">Our mission</h1>
          <p class="lead">
            In the challenging environment of the clinical research industry, our top priority is to provide the highest
            quality in a timely manner. Yet, that’s not the limit. Our team of experts is dedicate to supporting our
            customers to bring the change that actually matters.
          </p>
        </b-col>
      </b-row>
    </b-container>
    <!-- End Our mission-->

    <!-- Start Our Services -->
    <section id="our-services" class="p-5">
      <b-container class="pt-5">
        <b-row class="pt-5 d-flex">
          <div
            data-aos="fade-up"
            data-aos-duration="1100"
            class="col-lg-12 ms-lg-5r text-center p-5"
            style="background-color: #f5f8fb; border-radius: 1rem"
          >
            <h1 class="fw-bold">Our Services</h1>
            <p class="b-5">
              Our team of experts is here to fulfill your needs. Whether you are short on human resources and need
              <br />
              just one programmer to get through the peak season or an entire team for long term allocation, we are
              <br />
              happy to provide you with our expertise.
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
        <b-col v-for="report in reporting" :key="report.title" class="text-center align-items-stretch mb-4">
          <div class="p-5 shadow-lg rounded-4 radius-1 h-100">
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
        <b-col lg="4" md="6" class="text-center align-items-stretch">
          <b-jumbotron id="orange" class="rounded-hover bg-light m-5 p-5 h-75">
            <div class="icon-box align-items-center">
              <div class="icon my-3">
                <div class="icon-bg-circle icon-bg-orange">
                  <img class="icon-img-center" src="images/Clinical Study Database Creation and Support.png" alt="" />
                </div>
              </div>
              <h5>Clinical Study Database Creation and Support</h5>
            </div>
          </b-jumbotron>
        </b-col>
        <b-col lg="4" md="6" class="text-center align-items-stretch">
          <b-jumbotron id="blue" class="rounded-hover bg-light m-5 p-5 h-75">
            <div class="icon my-3">
              <div class="icon-bg-circle icon-bg-blue">
                <img class="icon-img-center" src="images/Data Entry.png" alt="" />
              </div>
            </div>
            <h5>Data Entry</h5>
          </b-jumbotron>
        </b-col>
        <b-col lg="4" md="6" class="text-center align-items-stretc h">
          <b-jumbotron id="purple" class="rounded-hover bg-light m-5 p-5 h-75">
            <div class="icon my-3">
              <div class="icon-bg-circle icon-bg-purple">
                <img class="icon-img-center" src="images/Data Validation With Edit Checking.png" alt="" />
              </div>
            </div>
            <h5>Data Validation With Edit Checking</h5>
          </b-jumbotron>
        </b-col>
        <b-col lg="4" md="6" class="mb-5 text-center align-items-stretch">
          <div id="purple" class="rounded-hover bg-light m-5 p-5 h-75">
            <div class="icon my-3">
              <div class="icon-bg-circle icon-bg-purple">
                <img class="icon-img-center" src="images/Discrepancy and Query Management.png" alt="" />
              </div>
            </div>
            <h5>Discrepancy and Query Management</h5>
          </div>
        </b-col>
        <b-col lg="4" md="6" class="mb-5 text-center align-items-stretch">
          <div id="orange" class="rounded-hover bg-light m-5 p-5 h-75">
            <div class="icon my-3">
              <div class="icon-bg-circle icon-bg-orange">
                <img class="icon-img-center" src="images/Laboratory Data Reconciliation.png" alt="" />
              </div>
            </div>
            <h5>Laboratory Data Reconciliation</h5>
          </div>
        </b-col>
        <b-col lg="4" md="6" class="mb-5 text-center align-items-stretch">
          <div id="blue" class="rounded-hover bg-light m-5 p-5 h-75">
            <div class="icon my-3">
              <div class="icon-bg-circle icon-bg-blue">
                <img class="icon-img-center" src="images/MedDRA and WHODrug Coding.png" alt="" />
              </div>
            </div>
            <h5>MedDRA and WHODrug Coding</h5>
          </div>
        </b-col>
      </b-row>
    </b-container>
    <!-- End Data Managment -->

    <!-- Start Terapeutic Areas -->

    <div
      class="bg-image img-fluid"
      style="background-image: url('images/terapeutic.png'); width: auto; height: 110vh; background-repeat: no-repeat"
    ></div>

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
    <b-container>
      <b-row id="join-us" class="text-center p-5">
        <b-col>
          <h1>Join Armat</h1>
          <p>We are constantly looking for talent and we want to see it flourish.</p>
        </b-col>
      </b-row>
      <b-row id="learn" class="img-responsive bg-image text-center p-5">
        <b-col cols="12">
          <span class="text align-self-end p-3">
            Whether you are an industry veteran or just making your first steps in biotechnology, we are waiting for you
            at Armat! Newbies can benefit from our special training programs which will help them build up the ladder.
            Whilst, more experienced candidates will directly work with the top pharma and get exposure to new market
            challenges. Regardless of the choice, your professional growth is guaranteed with us.
          </span>
          <div class="col align-item-center p-5">
            <button type="button" class="btn btn-primary btn-lg">Learn More</button>
          </div>
        </b-col>
      </b-row>
    </b-container>
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
      let reportingContents = await $content('services/reporting').fetch()
      reporting = _.orderBy(reportingContents, 'sortkey')
      console.log(reporting)
    } catch (e) {
      error({ message: 'Reporting not found' })
    }
    return { reporting }
  },
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
  letter-spacing: 0.02rem;
  font-weight: 400;
}

#our-services h1 {
  font-size: 44px;
  font-weight: 700;
  color: #263e52;
}

#our-services p {
  font-size: 20px;
  font-weight: 400;
  color: #263e52;
}

#reporting h1 {
  font-size: 42px;
  font-weight: 600;
  color: #263e52;
}

#reporting p {
  font-size: 20px;
  letter-spacing: 0.02rem;
  font-weight: 400;
}

#data h1 {
  font-size: 42px;
  font-weight: 600;
  color: #263e52;
}

#data p {
  font-size: 20px;
  letter-spacing: 0.02rem;
  font-weight: 400;
}

.radius-1 {
  border-radius: 1.5rem;
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

.icon-bg-orange {
  background-color: #f6bc84;
}

.icon-bg-blue {
  background-color: #8dbef8;
}

.icon-bg-purple {
  background-color: #c5b5e3;
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

#blue.rounded-hover:hover {
  -webkit-box-shadow: 0px 0px 0px 3px var(--cornflowerblue-color);
  -moz-box-shadow: 0px 0px 0px 3px var(--cornflowerblue-color);
  box-shadow: 0px 0px 0px 3px var(--cornflowerblue-color);
  transition: 0.4s;
  cursor: pointer;
}

#orange.rounded-hover:hover {
  -webkit-box-shadow: 0px 0px 0px 3px #f49235;
  -moz-box-shadow: 0px 0px 0px 3px #f49235;
  box-shadow: 0px 0px 0px 3px #f49235;
  transition: 0.4s;
  cursor: pointer;
}

#purple.rounded-hover:hover {
  -webkit-box-shadow: 0px 0px 0px 3px #af98d9;
  -moz-box-shadow: 0px 0px 0px 3px #af98d9;
  box-shadow: 0px 0px 0px 3px #af98d9;
  transition: 0.4s;
  cursor: pointer;
}

/* border hover end */
</style>