<template>
  <div class="main">
    <b-row>
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
        <div class="search-box my-4">
          <input type="text" class="search" placeholder="Enter name of the city">
          <button class="search-btn">Enter</button>
        </div>
        <h4 class="table-heading mb-4">Most popular cities</h4>
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
        <footer class="desktop-footer">
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
      <b-col md="6" class="image-column">
        <img src="../assets/free-shipping 1.png" alt="" class="car-img">
        <img src="../assets/Vector 1.png" alt="" class="road-img">
        <img src="../assets/Vector 2.png" alt="" class="peshehod">
        <h4 class="img-title">Fast Service</h4>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700&display=swap');

html, * {
  font-family: 'Roboto', sans-serif;
}

.main {
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

.search-box {
  height: 60px;
  overflow: hidden;
}

.search {
  background: #FFFFFF;
  border: 1px solid #E9F0EB;
  box-sizing: content-box;
  border-radius: 50px;
  height: 90%;
  width: 65%;
  padding-left: 30px;
  font-weight: 700;
  font-size: 24px;
  color: #283044;
  border-right: none;
  padding-top: 0px;
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
  height: 100%;
  margin-left: -100px;
  box-sizing: border-box;
  font-weight: 700;
  text-transform: uppercase;
  size: 24px;
  color: #FFFFFF;
  border: none;
}

.image-column {
  overflow: hidden;
  position: relative;
  background-color: #F7F7F7;
  border-radius: 40px 0px 0px 40px;
  height: 100vh;
}

.car-img {
  position: absolute;
  z-index: 10;
}

.road-img {
  position: absolute;
  z-index: 7;
}

.peshehod {
  position: absolute;
  z-index: 8;
}

.img-title {
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

.desktop-footer {
  position: absolute;
  bottom: 10px;
}

.desktop-footer {
  size: 14px;
  color: #283044;
  opacity: 0.5;
}
.payment-images{
  
}

</style>
