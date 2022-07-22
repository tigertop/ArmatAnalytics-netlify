<template>
  <div>
    <div id="submit-wrap" v-for="(elem, index) in submitWrap" :key="index">
      <section class="img-overlay-color" :style="{ '--overlaycolor': elem.color }">
        <b-container fluid class="bv-row bv-row-flex-cols pt-5 img-responsive">
          <b-row class="text-center pt-5">
            <b-col align-self="center" cols="12" class="text">
              <div>
                <span class="pt-lg-5 wrap-body">Here will be dynamic vacancy name</span>
              </div>
            </b-col>
          </b-row>
        </b-container>
        <div class="img-responsive-wrap" :style="{ backgroundImage: 'url(' + elem.image + ')' }"></div>
      </section>
    </div>
    <!-- Application form Start -->
    <b-container fluid="sm" class="submit-container py-5">
      <b-card class="border-0 shadow" style="border-radius: 10px;">
        <b-card-body>
          <b-row class="my-5">
            <b-col col lg="6" md="6" sm="6">
              <b-form-input id="input-large" size="lg" type="text" placeholder="Name"></b-form-input>
            </b-col>
            <b-col col lg="6" md="6" sm="6">
              <b-form-input id="input-large" size="lg" type="text" placeholder="Surname"></b-form-input>
            </b-col>
          </b-row>
          <b-row class="my-5">
            <b-col col lg="12" md="12" sm="12">
              <b-form-input id="input-large" size="lg" v-model="phone" placeholder="Phone Number"></b-form-input>
            </b-col>
          </b-row>
          <b-row class="my-5">
            <b-col col lg="12" md="12" sm="12">
              <b-form-input id="input-live" size="lg" v-model="email" placeholder="Email" trim></b-form-input>
            </b-col>
          </b-row>
          <b-row class="my-5">
            <b-col col lg="12" md="12" sm="12">
              <p class="font-weight-bold">If there is anything you would like us to know, please write below:</p>
              <b-form-textarea
                rows="8"
                id="input-live"
                size="lg"
                placeholder="Message (Please type your inquiry in detail.) "
                trim
              ></b-form-textarea>
            </b-col>
          </b-row>
          <b-row class="my-5">
            <b-col col lg="12" md="12" sm="12">
              <b-form-file id="input-file" size="lg"></b-form-file>
            </b-col>
          </b-row>
          <recaptcha />
          <b-row class="my-5">
            <b-col col lg="12" md="12" sm="12">
              <b-button type="submit" class="w-100" size="lg" variant="primary">Apply</b-button>
            </b-col>
          </b-row>
        </b-card-body>
      </b-card>
    </b-container>
    <!-- Application form End -->
  </div>
</template>

<script>
import _ from 'lodash'
export default {
  name: 'SubmitPage',
  async asyncData({ $content }) {
    let submitWrap = await $content('submitwrap').fetch()

    return {
      submitWrap,
    }
  },
}
</script>

<style>
.wrap-body {
  font-family: 'Source Sans Pro', sans-serif;
  font-size: 2.8em;
  color: white;
  font-weight: 600;
}

.img-overlay-color {
  background-color: var(--overlaycolor);
  height: 35vh;
  position: relative;
  opacity: 0.9;
}

.img-responsive-wrap {
  position: absolute;
  left: 0;
  top: 0;
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center;
  width: 100%;
  height: 35vh;
  opacity: 0.2;
}

.wrap-body {
  z-index: 99;
  position: relative;
}

.submit-container {
  max-width: 700px;
}
</style>