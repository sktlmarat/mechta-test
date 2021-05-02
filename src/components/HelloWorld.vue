<template>
  <div class="main">
    <b-row class="row">
      <b-col md="1"></b-col>
      <b-col md="5">
        <div>
          <b-navbar variant="faded" type="light">
            <b-navbar-brand href="#" class="nav-brand">
              <img src="../assets/xing 1.png" class="d-inline-block align-top" alt="Kitten">
              <span>FastService</span>
            </b-navbar-brand>
          </b-navbar>
        </div>
        <h1 class="main-heading mt-5">Delivery cost</h1>
        <p class="main-subheading">Enter name of the city to count delivery cost</p>
        <input type="text" :class="!this.error ? 'search mt-4' : 'search-error mt-4'" placeholder="Enter name of the city" v-model="city" @keyup.enter="search">
        <button :class="!this.error ? 'search-btn' : 'error-btn'" @click="search">Enter</button>
        <p class="error mt-1" v-if="this.error">{{ this.error }}</p>
        <h4 class="table-heading my-4">Most popular cities</h4>
        <div class="table-row">
          <div class="table-col">
            <span>Nur-Sultan</span>
            <span>Zhana Turmis</span>
          </div>
          <div class="table-col">
            <span>Almaty</span>
            <span>Karaganda</span>
          </div>
          <div class="table-col">
            <span>Shymkent</span>
            <span>Kentau</span>
          </div>
          <div class="table-col">
            <span>Atyrau</span>
            <span>Aitei</span>
          </div>
          <div class="table-col">
            <span>Aktau</span>
            <span>Pavlodar</span>
          </div>
        </div>
        <footer class="desktop-footer mt-5">
          <span>All rights reserved</span>
          <br>
          <span>Fast service 2021</span>
          <div class="payment-images">
            <img src="../assets/1200px-Maestro_2016.png" alt="">
            <img src="../assets/1280px-Mastercard-logo.png" alt="">
            <img src="../assets/logo.png" alt="">
            <img src="../assets/visa-logo-icon-png_44632.png" alt="">
          </div>
        </footer>
      </b-col>
      <b-col md="6" class="deliveries" v-if="this.deliveries && !this.error">
        <b-card img-right v-for="delivery in deliveries" :class="delivery.available ? 'delivery' : 'delivery unavailable'">
          <h3>{{ delivery.type }}</h3>
          <p v-if="!delivery.available">Not available in that city</p>
          <h4>{{ delivery.price }}$</h4>
        </b-card>
      </b-col>
      <b-col md="6" class="image-column" v-else>
        <img src="../assets/free-shipping 1.png" alt="" class="car-img">
        <img src="../assets/Vector 1.png" alt="" class="road-img">
        <img src="../assets/Vector 2.png" alt="" class="peshehod">
        <h4 class="img-title">Fast <br>Service</h4>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  data() {
    return {
      city: null,
      deliveries: null,
      error: null
    }
  },
  mounted() {

  },
  methods: {
    async search() {
      try {
        const response = await fetch(`https://qvjgl.mocklab.io/delivery/check?search=${this.city.toLowerCase()}`);
        const result = await response.json();
        this.deliveries = result;
        this.error = null;
      } catch (e){
        this.error = ("We didn't found such city. Please check spelling");
      }
    },
    wipe() {
      this.error = null;
      this.city = null;
    }
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700&display=swap');

html, * {
  font-family: 'Roboto', sans-serif;
}

html {
  overflow-y: scroll;
}

.error{
  font-weight: normal;
  font-size: 16px;
  color: #FF4757;
}
.error-btn{
  background: linear-gradient(279.56deg, #FF4757 15.15%, rgba(255, 255, 255, 0) 171.55%);
  border-radius: 50px;
  width: 25%;
  height: 65px;
  margin-left: -50px;
  box-sizing: border-box;
  font-weight: 700;
  text-transform: uppercase;
  size: 24px;
  color: #FFFFFF;
  border: none;
  vertical-align: middle;
  transform: translateY(-3px);
}

.nav-brand span {
  size: 24px;
  line-height: 40px;
  color: #283044;
  margin-left: 8px;
}

.main-heading {
  size: 48px;
  font-weight: 700;
  color: #283044;
}

.main-subheading {
  size: 24px;
  font-weight: 400;
  color: rgba(40, 48, 68, 0.5);
}


.search {
  background: #FFFFFF;
  border: 1px solid #E9F0EB;
  box-sizing: border-box;
  border-bottom-left-radius: 50px;
  border-top-left-radius: 50px;
  border-right: none;
  height: 65px;
  width: 65%;
  padding-left: 30px;
  font-weight: 700;
  font-size: 24px;
  color: #283044;
  padding-top: 0px;
  padding-right: 50px;
}
.search-error{
  border: 1px solid #FF4757;
  background: #FFFFFF;
  box-sizing: border-box;
  border-bottom-left-radius: 50px;
  border-top-left-radius: 50px;
  border-right: none;
  height: 65px;
  width: 65%;
  padding-left: 30px;
  font-weight: 700;
  font-size: 24px;
  color: #283044;
  padding-top: 0px;
  padding-right: 50px;
  outline: none;
}

.search:focus {
  outline: none;
}

.table-heading {
  font-weight: 400;
  size: 24px;
}

.search::placeholder {
  font-size: 20px;
  color: #D9E4DC;
  font-weight: normal;
}

.search-btn {
  background: linear-gradient(279.56deg, #65B3E4 15.15%, rgba(120, 161, 187, 0) 171.55%);
  border-radius: 50px;
  width: 25%;
  height: 65px;
  margin-left: -50px;
  box-sizing: border-box;
  font-weight: 700;
  text-transform: uppercase;
  size: 24px;
  color: #FFFFFF;
  border: none;
  vertical-align: middle;
  transform: translateY(-3px);
}
.deliveries{
  background-color: #F7F7F7;
  border-radius: 40px 0px 0px 40px;
}
.unavailable h3,h4{
  opacity: 50%;
}

.image-column {
  position: relative;
  background-color: #F7F7F7;
  border-radius: 40px 0px 0px 40px;
  height: 97vh;
  overflow: hidden;
  padding: 0px;
  margin: 0px;
  border: none;
}

.car-img {
  left: 100px;
  position: absolute;
  z-index: 10;
  height: 450px;
  width: 450px;
  top: 100px;
}

.road-img {
  left: 100px;
  top: 50px;
  position: absolute;
  z-index: 7;
}

.peshehod {
  left: 100px;
  top: 250px;
  position: absolute;
  z-index: 8;
}

.img-title {
  font-size: 75px;
  left: 390px;
  top: 20px;
  color: rgba(40, 48, 68, 0.1);
  position: absolute;
  z-index: 9;
}

.nav-brand {
  font-weight: 700;
}

.table-col span {
  padding-left: 10px;
  width: 40%;
  display: inline-block;
  font-weight: normal;
  size: 20px;
  color: rgba(40, 48, 68, 0.5);
  border-bottom: 1px solid #E9F0EB;
  margin-right: 10%;
  padding-bottom: 5px;
  padding-top: 10px;
}
.delivery{
  width: 60%;
  margin-left: 10%;
  margin-top: 5%;
  background: #FFFFFF;
  border-radius: 22px;
  border: none;
  height: 25%;
}
.delivery h3{
  text-transform: capitalize;
  color: #283044;
  font-size: 30px;
  font-weight: bold;
}
.delivery h4{
  color: #78A1BB;
  font-size: 40px;
  font-weight: bold;
}
.delivery p{
  color: #283044;
  opacity: 50%;
  font-size: 20px;
}
.desktop-footer {
  size: 14px;
  color: #283044;
  opacity: 0.5;
}

.payment-images {
  float: right;
  padding-right: 10%;
}
.payment-images img{
  margin-left: 10px;
}


</style>
