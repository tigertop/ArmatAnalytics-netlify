<template>
  <!-- Start Navbar -->
   <b-container>
  <b-navbar
    class="nav-links bg-white "
    toggleable="lg"
    type="light"
    sticky="true"
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
        <b-nav-item href="/CareersPage">Careers</b-nav-item>
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
  name: "AppHeader",
};
</script>

<style>
:root {
  --cornflowerblue-color: #72aff7;
  --midnightblue-color: #013164;
  --darkturquoise-color: #00b6e0;
  --darkslategray-color: #25546d;
  --mediumturquoise-color: #37bfef;
  --ghostwhite-color: #f9fbfc;
  --lightsteelblue-color: #c2b6e5;
  --white-color: #ffffff;
  --navy-color: #25546d;
  --darkerblue-color: #263e52;
  --justsky-color: #f5f8fb;
}

.navbar .nav-item {
  margin: 0 !important;
  padding: 0 !important;
}

.navbar .main-btn {
  background-color: var(--cornflowerblue-color);
  margin: 10px 10px 10px;
  padding: 10px 10px 10px;
  border-radius: 10px;
  border-color: var(--cornflowerblue-color);
  text-decoration: none;
  color: var(--white-color);
  font-size: 18px;
  font-weight: 700;
  display: inline-block;
}

.navbar .nav-item a {
  font-size: 18px;
  font-weight: 400;
  color: var(--navy-color) !important;
  margin: 20px 30px 0;
  padding: 0px;
}

.navbar .nav-item .active {
  font-size: 18px;
  font-weight: 700;
  color: var(--navy-color);
  margin: 20px 30px 0;
  padding: 0px;
}

.navbar .active::after {
  content: "";
  width: 8px;
  height: 8px;
  background: var(--cornflowerblue-color);
  display: block;
  margin: auto;
  border-radius: 50%;
}

.nav-links ul li .nav-link::after {
  content: "";
  width: 0%;
  height: 2px;
  background: var(--cornflowerblue-color);
  display: block;
  margin: auto;
  transition: 0.5s;
}

.nav-links ul li:not(.active) .nav-link:hover::after {
  width: 100%;
}

.main-btn:hover {
  background: #013164;
  border-color: #013164;
  transition: all 0.25s ease-in-out;
}
</style>
