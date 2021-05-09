<template>
  <div id="navbar" class="navContainer">
      <div class="col-12 p-0">

        <div class="navBar">

          <div class="navBrand">
            <a href="/">
              <img src="../assets/images/Mechagon_Logo_B&W.svg" alt="Mechagon logo" />
            </a>
          </div>

          <div class="nav-wrapper">
            <div class="nav">
              <a href="/" class="navLink">Dash</a>
              <a href="/products" class="navLink">Products</a>
              <a href="/profile" class="navLink">My Profile</a>
              <a href="/about" class="navLink">About</a>
              <a href="/cart" class="navLink">
                <i class="fas fa-shopping-cart cart-icon-bg"></i>
                <span class="count-cart">0</span>
              </a>
              <!-- <div class="navLink p-0"><AuthNav /></div> -->
            </div>
          </div>

        </div>

        <div class="navBar-mobile">

          <div class="navBrand">
            <a href="/">
              <img src="../assets/images/Mechagon_Logo_B&W.svg" alt="Mechagon logo" />
            </a>
          </div>

          <div>
            <div class="navHamburger" @click="hideMenuButton" v-if="menuButtonDisplays">Menu</div>
            <div class="navHamburger" @click="hideCloseButton" v-if="closeButtonDisplays">X</div>
          </div>

          <div class="nav-mobile w-100" v-if="mobileNavDisplays">
            <a href="/" class="navLink">Dash</a>
            <a href="/products" class="navLink">Products</a>
            <a href="/profile" class="navLink">My Profile</a>
            <a href="/about" class="navLink">About</a>
            <a href="/cart" class="navLink"><i class="fas fa-shopping-cart"></i><span class="count-cart">0</span></a>
            <!-- <div class="navLink"><AuthNav /></div> -->
          </div>

        </div>
      </div>
    </div>
</template>

<script>
import { ref } from 'vue';

export default {
  name: 'Navbar',
  setup() {
    const closeButtonDisplays = ref(false);
    const menuButtonDisplays = ref(true);
    const mobileNavDisplays = ref(false);

    function toggleMobileNav() {
      mobileNavDisplays.value = !mobileNavDisplays.value;
    }

    function hideCloseButton() {
      closeButtonDisplays.value = false;
      menuButtonDisplays.value = true;
      toggleMobileNav();
    }

    function hideMenuButton() {
      closeButtonDisplays.value = true;
      menuButtonDisplays.value = false;
      toggleMobileNav();
    }

    return {
      closeButtonDisplays,
      menuButtonDisplays,
      hideMenuButton,
      hideCloseButton,
      mobileNavDisplays,
    };
  },
}
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css?family=Roboto+Condensed');
@import url('https://fonts.googleapis.com/css?family=Share+Tech');

.cart-icon-bg {
  background-color: #000896;
}

.count-cart {
    padding: 0 5px;
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
  padding: 10px;
}

.navContainer {
  background-color: #000896;
}

.navHamburger {
  background-color: #fff;
  border: solid 1px #888;
  border-radius: 7px;
  color: #000;
  font-family: 'Roboto', sans-serif;
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
  transition-duration: .4s;
}

.navLink {
  color: #fff;
  cursor: pointer;
  display: block;
  font-size: 18px;
  padding: 10px 1.5rem;
}

.navLink:hover {
  color: #00ff04;
  text-decoration: none;
  transition-duration: .4s;
}

.nav-mobile {
  flex-direction: column;
}

@media (max-width:991px) {
  .navBrand img {
    height: 60px;
  }

  .navLink {
    font-size: 18px;
    padding: 10px 15px;
  }
}

@media (max-width:767px) {
  .navBrand img {
    height: 50px;
  }

  .navLink {
    font-size: 16px;
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
