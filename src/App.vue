<template>
  <div id="app">
    <b-navbar toggleable="lg">
      <b-navbar-brand href="/">
        <img src="@/assets/piedpiperlogo.svg" class="d-inline-block align-top piedpiperlogo" alt="PiedPiperCoin">
      </b-navbar-brand>

      <!-- <b-nav-text class="follow"><h2>FOLLOW @PIEDPIPERCOIN FOR UPDATES</h2></b-nav-text> -->

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <!-- <b-navbar-nav>
          <b-nav-item href="#">Link</b-nav-item>
          <b-nav-item href="#" disabled>Disabled</b-nav-item>
        </b-navbar-nav> -->

        <!-- Right aligned nav items -->
        <b-navbar-nav class="ml-auto">
          <b-navbar-nav>
            <li class="nav-item">
              <b-link to="/" class="nav-link">Home</b-link>
            </li>
            <li class="nav-item">
              <b-link to="exchanges" class="nav-link">Exchanges</b-link>
            </li>
          </b-navbar-nav>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>

    <router-view/>

    <hr>

    <footer class="">
      <div class="container">
        <p class="float-right">
          <a href="https://twitter.com/piedpipercoin">@piedpipercoin</a>
        </p>
        <p>Disclaimer: PiedPiperCoin is Not affiliated with HBO or Silicon Valley</p>
      </div>
    </footer>
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css?family=Roboto&display=swap");
@import url("https://fonts.googleapis.com/css?family=Roboto+Slab&display=swap");

body {
  background: url('https://www.piedpipercoin.com/img/pied-piper-bridge.31dc61a8.jpg') no-repeat center center fixed;
  -webkit-background-size: cover;
  -moz-background-size: cover;
  background-size: cover;
  -o-background-size: cover;
}

#app {
  font-family: "Roboto slab", "sans-serif";
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #ffffff;
}

footer {
  color: #217f51;
}
// body,
// span.navbar-text {
//   color: #ffffff!important;
// }

// nav.navbar {
//   background-color: #007045;
// }

.piedpiperlogo {
  width: 62px;
}

a {
  color: #217f51;
}

hr {
  border-top: 1px solid #217f51;
}

.navbar-light .navbar-nav .nav-link {
  color: #217f51;
}

.navbar-light .navbar-nav .nav-link:focus, 
.navbar-light .navbar-nav .nav-link:hover {
  color: #FFFFFF;
}
</style>
