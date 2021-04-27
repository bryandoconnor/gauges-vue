<template>
  <div id="navbar" class="row">
      <div class="col-12 mb-5">

        <div class="navBar">

          <div class="navBrand">
            <a href="/">
              <img src="../assets/images/Mechagon_Logos-02.svg" alt="Mechagon logo" />
            </a>
          </div>

          <div class="nav-wrapper">
            <div class="nav">
              <a href="/" class="navLink">Dash</a>
              <a href="/products" class="navLink">Products</a>
              <a href="/profile" class="navLink">My Profile</a>
              <a href="/about" class="navLink">About</a>
              <a href="/cart" class="navLink"><i class="fas fa-shopping-cart"></i><span class="count-cart">0</span></a>
              <div class="navLink p-0"><AuthNav /></div>
            </div>
          </div>

        </div>

        <div class="navBar-mobile">

          <div class="navBrand">
            <a href="/">
              <img src="../assets/images/Mechagon_Logos-02.svg" alt="Mechagon logo" />
            </a>
          </div>

          <div style={menuStyle.displays.menuDisplay}>
            <div class="navHamburger" onClick={clickMenu}>Menu</div>
          </div>
          <div style={closeStyle.displays.closeDisplay}>
            <div class="navHamburger" onClick={clickClose}>X</div>
          </div>

          <div class="nav-mobile w-100" style={navStyle.displays.navDisplay}>
            <a href="/" class="navLink">DASH</a>
            <a href="/products" class="navLink">PRODUCTS</a>
            <a href="/profile" class="navLink">MY PROFILE</a>
            <a href="/about" class="navLink">ABOUT</a>
            <a href="/cart" class="navLink"><i class="fas fa-shopping-cart"></i><span class="count-cart">0</span></a>
            <div class="navLink"><AuthNav /></div>
          </div>

        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'Navbar',
  // components: { VueGauge }
  setup() {
    return {
      Quantity: 20
    }
  },
}
</script>

<style scoped>
.count-cart {
    padding: 0 5px;
}

.nav {
  display: -webkit-flex;
  display: flex;
  -webkit-flex-wrap: wrap;
  flex-wrap: wrap;
  padding-left: 0;
  margin-bottom: 0;
  list-style: none;
}

.navBar {
  align-items: center;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  margin: 0 20px;
  padding: 2px 4px;
  position: relative;
}

.navBar-mobile {
  display: none;
}

.navBrand img {
  height: 70px;
}

.navContainer {
  background-color: #0d84a8;
  margin-bottom: 30px;
}

.navHamburger {
  background-color: #fff;
  border: solid 1px #888;
  border-radius: 7px;
  color: #000;
  font-family: 'Permanent Marker', cursive;
  margin: 0 20px;
  padding: 5px 10px;
}

.navHamburger:hover {
  background-color: #ff9406;
  border: none;
  border-radius: 7px;
  color: #fff;
  cursor: pointer;
  padding: 5px 10px;
  transition-duration: .8s;
}

.navLink {
  background-color: transparent;
  color: #000;
  cursor: pointer;
  display: block;
  font-size: 14px;
  font-family: 'Helvetica', sans-serif;
  padding: 10px 1.5rem;
  text-shadow: 0 2px 0 rgba(255, 255, 255, .5);
}

.navLink:hover {
  color: #ff9406;
  text-decoration: none;
  transition-duration: .8s;
}

.nav-mobile {
  flex-direction: column;
}

@media (max-width:991px) {
  .navBrand img {
    height: 60px;
  }

  .navLink {
    font-size: 12px;
    padding: 10px 15px;
  }
}

@media (max-width:767px) {
  .navBrand img {
    height: 50px;
  }

  .navLink {
    font-size: 11px;
    padding: 10px 5px;
  }
}

@media (max-width:575px) {
  .navBar {
    display: none;
  }

  .navBar-mobile {
    align-items: center;
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    margin: 0 20px;
    padding: 2px 4px;
    position: relative;
  }

  .navLink {
    font-size: 14px;
    padding: 10px 1.5rem;
  }
}
</style>