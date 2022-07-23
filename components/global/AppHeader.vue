<template>
 <!-- Start Navbar -->
 <b-container>
  <b-navbar
    id="navbar"
    class="bg-white "
    toggleable="lg"
    type="light"
  >
    <b-navbar-brand href="#">
      <b-img
        class="img mb-2"
        src="~/static/images/Layer2.svg"
        alt="logo"
      ></b-img>
    </b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto">
        <b-nav-item class="active" href="/">Home</b-nav-item>
        <b-nav-item href="/careers">Careers</b-nav-item>
        <b-nav-item href="/#about">About us</b-nav-item>
        <b-nav-item href="#contact">Contact us</b-nav-item>
        <b-button class="main-btn" href="/CareersPage#root"
          >ROOT Program</b-button
        >
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
  </b-container>
  <!-- End Navbar -->
</template>

<script>
export default {
  name: 'AppHeader',
}
</script>

<style>
#navbar .nav-item {
  margin: 0 !important;
  padding: 0 !important;
}

#navbar .main-btn {
  background-color: #72aff7!important;
  margin: 10px 10px 10px !important;
  padding: 10px 10px 10px !important;
  border-radius: 10px !important;
  border-color: #72aff7 !important;
  text-decoration: none !important;
  color: #ffffff !important;
  font-size: 18px !important;
  font-weight: 700 !important;
  display: inline-block !important;
}

#navbar .nav-item a {
  font-size: 18px!important;
  font-weight: 400;
  color: #25546d !important;
  margin: 20px 30px 0!important;
  padding: 0px!important;
}

#navbar .nav-item .active {
  font-weight: 700!important;
}

#navbar .active::after {
  content: ''!important;
  width: 8px!important;
  height: 8px!important;
  background: #72aff7!important;
  display: block!important;
  margin: auto!important;
  border-radius: 50%!important;
}

#navbar ul li .nav-link::after {
  content: ''!important;
  width: 0%;
  height: 2px!important;
  background: #72aff7!important;
  display: block!important;
  margin: auto!important;
  transition: 0.5s!important;
}

#navbar ul li:not(.active) .nav-link:hover::after {
  width: 100%!important;
}

#navbar .main-btn:hover {
  background: #013164!important;
  border-color: #013164!important;
  transition: all 0.25s ease-in-out!important;
}
</style>
