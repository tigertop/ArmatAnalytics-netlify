<template>
  <footer id="footer">
    <b-container>
      <b-row>
        <b-col
          md="4"
          lg="4"
          sm="12"
          class="text-lg-left text-md-left text-center"
        >
          <b-link to="/" class="d-inline-block mx-auto">
            <b-img
              class="img"
              src="~/static/images/footer.png"
              alt="logo"
            ></b-img>
          </b-link>
        </b-col>
        <b-col md="4" lg="4" sm="12" class="text-center mt-2">
          <ul class="list-unstyled d-flex justify-content-between">
            <li><b-link to="/" exact>Home</b-link></li>
            <li><b-link to="/careers">Careers</b-link></li>
            <li><b-link to="/#about">About us</b-link></li>
            <li><b-link to="#contact">Contact us</b-link></li>
          </ul>
        </b-col>
        <b-col
          md="4"
          lg="4"
          sm="12"
          class="text-lg-right text-md-right text-center mt-2"
        >
          <a>© 2022. All rights reserved.</a>
        </b-col>
      </b-row>
    </b-container>
  </footer>
</template>

<script>
export default {
  name: "AppFooter",
};
</script>

<style>
#footer {
  background-image: url("~/static/images/Group12.png");
  padding: 1rem;
}

#footer a {
  font-size: 16px;
  opacity: 0.6;
  font-weight: 200;
  color: #ffffff !important;
}
</style>
