<template>
  <div id="home" class="">
    <div class="absolute top-[0] grid grid-cols-1 md:grid-cols-2 items-center h-full">
      <div class="w-full pl-14">
        <h1
          class=" text-white text-4xl sm:text-5xl lg:text-6xl lg:w-[400px] xl:w-full font-black animate__animated animate__fadeInLeft">
          We can fix it <br class="text-white hidden 2xl:inline-block">
          easy,
          <span class="text-white-tint">Your Car, Our Expertise</span>
        </h1>
        <p
          class="text-base sm:text-lg w-full sm:w-[380px] lg:w-[400px] xl:w-[450px] text-white-tint pt-7 sm:pt-10 animate__animated animate__fadeInLeft animate__delay-1s">
          Mechanics that Think Outside the Engine, Fix It Quick, Get Your Ride in the Thick.
        </p>
      </div>
    </div>
    <!--  copied -->
    <div class="offers-section w-full">
      <div class="container offers-container">
        <div id="cphContent_OffersSection" class="row">
          <div class="col-xs-12 offers-col">
            <div class="offer"><span> 3 year/36,000 mile <strong>Nationwide Warranty</strong></span></div>
            <div class="offer"><span> Free Local <strong>Shuttle Service</strong></span></div>
            <div class="offer"><span> Financing <strong>Available</strong></span></div>
            <div class="offer"><span> Loaner <strong>Cars</strong></span></div>
            <div class="offer"><span> Comfortable <strong>Waiting Area</strong></span></div>
          </div>
        </div>
      </div>
    </div>
  </div>
  <!--  -->
  <section>
    <ServicesComponent />
  </section>
  <section>
    <RateComponent />
  </section>
  <section>
    <OurserviceComponent />
  </section>
  <section>
    <CallbackComponent />
  </section>
  <section>
    <ReviewsComponents />
  </section>
</template>

<script lang="ts">
import { defineComponent } from 'vue'
import CallbackComponent from "../components/CallBackComponent.vue"
import navbarComponent from "../components/navbarComponent.vue"
import OurserviceComponent from '../components/OurserviceComponent.vue'
import RateComponent from "../components/RateComponent.vue"
import ReviewsComponents from "../components/ReviewsComponents.vue"
import ServicesComponent from "../components/ServicesComponent.vue"
export default defineComponent({
  name: "HomeView",
  components: {
    // navbarComponent,
    ServicesComponent,
    RateComponent,
    OurserviceComponent,
    ReviewsComponents,
    CallbackComponent,
  },
  setup() {


    return {}
  }
})
</script>

<style scoped>
#home {
  background: url("/src/assets/bg8.jpeg");
  /* height: 40%; */
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  /* height: fit-content; */
  background-color: blue;
  height: 100vh;
  width: 100vw;
}

@media (max-width: 1223px) {
  .offers-col {
    justify-content: space-around;
  }
}

.offers-section {
  /* position: absolute; */
}

@media (max-width: 1223px) {
  .offers-container {
    bottom: 0;
  }
}

@media (min-width: 992px) {
  .container {
    width: 964px;
  }
}

@media (min-width: 768px) {
  .container {
    width: 744px;
  }
}

.container {
  margin-right: auto;
  margin-left: auto;
  padding-left: 12px;
  padding-right: 12px;
}

.offers-container {
  position: absolute;
  bottom: 60px;
  left: 0;
  right: 0;
  z-index: 1;
  width: 100%
}

.offers-col {
  /* justify-content: space-around; */
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

@media (max-width: 1223px) {
  .offers-section .offer span strong {
    font-size: 20px;
  }
}

.row:before,
.row:after {
  content: " ";
  display: table;
}

.offers-section .offer span strong {
  display: block;
  font: inherit;
  font-size: 24px;
}

@media (max-width: 1223px) {
  .offers-section .offer {
    display: flex;
    flex-direction: column;
    justify-content: flex-end;
    margin-top: 15px;
    margin-bottom: 10px;
    padding-left: 25px;
    max-width: 100%;
    font-size: 1em;
  }
}


.offers-section .offer {
  counter-increment: count;
  display: inline-block;
  position: relative;
  padding-left: 45px;
  color: #fff;
  font: 400 1.125em / 1.2 'Rubik', Verdana, Sans-serif;
  vertical-align: top;
}

* {
  -webkit-box-sizing: border-box;
  -moz-box-sizing: border-box;
  box-sizing: border-box;
}

.offers-section .offer span {
  font: 400 1em / 1.2 'Rubik', Verdana, Sans-serif;
}

.offers-section .offer:after {
  content: '';
  display: block;
  margin-top: 15px;
  width: 110px;
  height: 3px;
  background: #fff;
}

.offers-section .offer:before {
  content: counter(count);
  display: inline-block;
  position: absolute;
  bottom: -4px;
  left: 10px;
  color: #fff;
  font: 400 1.125em / 1 'Rubik', Verdana, Sans-serif;
}

.offers-section .offer:nth-child(-n+9):before {
  content: '0' counter(count);
}

.row {
  margin-left: -12px;
  /* margin-right: -12px; */
}

.col-xs-12 {
  width: 100%;
}
</style>