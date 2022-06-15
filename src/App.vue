<template>
  <div class="session-1">
    <HeaderComponent />
    <BannerComponent />
    <ReviewComponent />
  </div>
  <OutstandingElements />
  <ReasonComponent />
  <RoadMapComponent />
  <FAQsComponent />
  <div class="session-3">
    <MediaShoutComponent />
    <PartnerComponent />
    <BackerComponent />
    <BackerComponent />
  </div>
  <FooterComponent />
</template>

<script setup>
import HeaderComponent from "./components/Header.vue";
import BannerComponent from "./components/Banner.vue";
import ReviewComponent from "./components/Review.vue";
import OutstandingElements from "./components/OutstandingElements.vue";
import ReasonComponent from "./components/ReasonComponent.vue";
import RoadMapComponent from "./components/RoadMap.vue";
import FAQsComponent from "./components/FAQs.vue";
import MediaShoutComponent from "./components/MediaShout.vue";
import PartnerComponent from "./components/Partner.vue";
import BackerComponent from "./components/Backer.vue";
import FooterComponent from "./components/Footer.vue";
import "bootstrap/dist/css/bootstrap.min.css";
import "bootstrap";
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.session-1 {
  background-image: url("./assets/final-bg-1.png");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  padding-bottom: 90px;
}
.session-3 {
  background-image: url("./assets/final-bg-6.png");
  background-repeat: no-repeat;
  background-size: 100% 100%;
  padding-bottom: 10px;
}
/* < PC */
@media(max-width: 992px) {
  .session-1, .session-3, .outstand-element {
    background-size: cover;
  }
  #reason {
    background-image: url('./assets/bg-1.png');
    background-size: cover;
  }
  #roadMap {
    background-size: cover;
  }
}
</style>
