<template>
  <div class="row text-center pt-2 pb-4 footer-bg">
    <div class="col-12 p-0">

      <div class="row mx-0 mt-2 mb-3">
        <div class="col-12 p-0">
          <a href="/" class="footer-link-basic footer-heading">
            <div class="row m-0">
              <div class="col-12 p-0 text-center">
                <img src="../assets/images/Mechagon_Logo_B&W.svg" alt="Mechagon logo" height="40" />
                <span class="d-inline-block ml-1 mr-3">|</span>© {{(new Date().getFullYear())}}
              </div>
            </div>
          </a>
        </div>
      </div>

      <div class="row m-0">
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-chart-line"></i>Dash
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-bomb"></i>Products
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-users-cog"></i>My Profile
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-coins"></i>About
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-shopping-cart"></i>Cart
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-bell"></i>Alerts
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-book-dead"></i>Reports
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-calendar-alt"></i>Calendar
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-cat"></i>Cats
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-chart-bar"></i>Charts
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-cocktail"></i>Cocktails
          </a>
        </div>
        <div class="col-4 col-md-3 py-3">
          <a href="/" class="footer-link-basic footer-links">
            <i class="mr-2 fas fa-comment"></i>FAQ
          </a>
        </div>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Share+Tech');

ul {
  list-style: none;
  margin: 0;
  padding: 0;
}

.footer-bg {
  background-color: #222;
}

.footer-heading {
  font-size: 22px;
}

.footer-links {
  font-size: 16px;
}

.footer-link-basic {
  color: #fff;
  font-family: 'Share Tech', sans-serif;
}

.footer-link-basic:hover {
  color: #00ff04;
  text-decoration: none;
  transition-duration: .4s;
}
</style>
