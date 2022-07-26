<template>
 <!-- Start Navbar -->
 <div class="bg-white">
  <b-container>
    <b-navbar
      id="navbar"
      class="bg-white sticky"
      toggleable="lg"
      type="light"
    >
      <b-navbar-brand href="/">
        <b-img
          class="img mb-2"
          src="~/static/images/Layer2.svg"
          alt="logo"
        ></b-img>
      </b-navbar-brand>
      <b-navbar-toggle class="navbar-toggler collapsed" target="nav-collapse">
        <span class="toggler-icon top-bar"></span>
        <span class="toggler-icon middle-bar"></span>
        <span class="toggler-icon bottom-bar"></span>
      </b-navbar-toggle>
      <b-collapse id="nav-collapse" is-nav>
        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/">Home</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/careers">Careers</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="/#about">About us</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link" to="#contact">Contact us</NuxtLink>
          </li>
          <b-button class="main-btn" href="/careers/#root">ROOT Program</b-button>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
    </b-container>
  <!-- End Navbar -->
  </div>
</template>

<script>
export default {
  name: 'AppHeader',
}
</script>

<style>
.sticky {
  position: sticky!important;
  top: 0px;
}

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
  font-weight: 400!important;
  color: #25546d !important;
  margin: 20px 30px 0!important;
  padding: 0px!important;
}

#navbar .nav-item .nuxt-link-exact-active {
  font-weight: 700!important;
}



@media only screen and (min-width: 992px) {
  #navbar ul li .nav-link:not(.nuxt-link-exact-active)::after {
    content: ''!important;
    width: 0%;
    height: 2px!important;
    background: #72aff7!important;
    display: block!important;
    margin: auto!important;
    transition: 0.5s!important;
  }
    #navbar .nuxt-link-exact-active::after {
    content: ''!important;
    width: 8px!important;
    height: 8px!important;
    background: #72aff7!important;
    display: block!important;
    margin: auto!important;
    border-radius: 50%!important;
  }
}



#navbar ul li .nav-link:not(.nuxt-link-exact-active):hover::after {
  width: 100%!important;
}

#navbar .main-btn:hover {
  background: #013164!important;
  border-color: #013164!important;
  transition: all 0.25s ease-in-out!important;
}

/* navbar toggler start */

.navbar-toggler {
  width: 35px;
  height: 20px;
  position: relative;
  transition: .5s ease-in-out;
}

.navbar-toggler,
.navbar-toggler:focus,
.navbar-toggler:active,
.navbar-toggler-icon:focus {
  outline: none;
  box-shadow: none;
  border: 0;
}

.navbar-toggler span {
  margin: 0;
  padding: 0;
}
.toggler-icon {
  display: block;
  position: absolute;
  height: 4px;
  width: 100%;
  background: var(--midnightblue-color) !important;
  border-radius: 2px;
  opacity: 1;
  left: 0;
  transform: rotate(0deg);
  transition: .33s ease-in-out;
}


.middle-bar {
  margin-top: 0px;
}

.navbar-toggler .top-bar {
  margin-top: 0px;
  transform : rotate(135deg);
}

.navbar-toggler .middle-bar {
  opacity: 0;
  filter: alpha(opacity=0);
}

.navbar-toggler .bottom-bar {
  margin-top: 0px;
  transform: rotate(-135deg);
}

.navbar-toggler.collapsed .top-bar {
  margin-top: -10px;
  transform: rotate(0deg);
}

.navbar-toggler.collapsed .middle-bar {
  opacity: 1;
  filter: alpha(opacity=100);
}

.navbar-toggler.collapsed .bottom-bar {
  margin-top: 10px;
  transform: rotate(0deg);
}

/* navbar toggler end */
</style>
