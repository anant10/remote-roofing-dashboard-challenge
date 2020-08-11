<template>
  <div id="app">
    <TopHeader />
    <div id="nav" class="second-header-2">
      <router-link to="/" class="second-header-3">Home</router-link>
      <router-link to="/about" class="second-header-3">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
import TopHeader from './components/TopHeader.vue';

export default {
  name: 'App',
  components: {
    TopHeader,
  },
};
</script>

<style>
#app {
  padding-left: 4%;
  padding-right: 4%;
  padding-top: 3%;
  padding-bottom: 5%;
  background-position: 0px 0px;
  background-size: cover;
  background-image: url('https://uploads-ssl.webflow.com/5f127ac8860f158e650f06b5/5f127dcece36df2cd5e4f713_Screen%20Shot%202020-07-17%20at%209.41.58%20PM.png');
}

.second-header-2 {
  /* padding-left: 10%;
  padding-right: 10%; */
  padding-top: 5%;
  padding-bottom: 5%;
  -webkit-box-pack: start;
  -webkit-justify-content: flex-start;
  -ms-flex-pack: start;
  justify-content: flex-start;
}

.second-header-3 {
  padding-left: 3%;
  padding-right: 7%;
  /* padding-top: 5%;
  padding-bottom: 5%; */

  font-family: AirbnbCerealLight, sans-serif;
  color: #fff;
  font-weight: 10%;
  font-size: 130%;
}
</style>
