<template>
  <div class="main">
    <b-row>
      <b-col md="2"></b-col>
      <b-col md="4">
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
        <input type="text" class="search my-4" placeholder="Enter name of the city">
        <button class="search-btn">Enter</button>
        <h4>Most popular cities</h4>
        <table>
          <tr>
          <td>Nur-Sultan</td>
          <td>Zhana Turmis</td>
          </tr>
          <tr>
            <td>Almaty</td>
            <td>Karaganda</td>
          </tr>
          <tr>
            <td>Shymkent</td>
            <td>Kentau</td>
          </tr>
          <tr>
            <td>Atyrau</td>
            <td>Aitei</td>
          </tr>
          <tr>
            <td>Aktau</td>
            <td>Pavlodar</td>
          </tr>
        </table>
        <footer>
          <span>All rights reserved</span>
          <br>
          <span>Fast service 2021</span>
          <img src="../assets/1200px-Maestro_2016.png" alt="">
          <img src="../assets/1280px-Mastercard-logo.png" alt="">
          <img src="../assets/logo.png" alt="">
          <img src="../assets/visa-logo-icon-png_44632.png" alt="">
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
html, *{
  font-family: 'Roboto', sans-serif;
}
.main{
  overflow: hidden;
  width: 100%;
  height: 100vh;
}
.nav-brand span{
  size: 24px;
  line-height: 40px;
  color: #283044;
  margin-left: 8px;
}
.main-heading{
  size: 48px;
  font-weight: 700;
  color: #283044;
}
.main-subheading{
  size: 24px;
  font-weight: 400;
  color: rgba(40, 48, 68, 0.5);
}
.search{
  background: #FFFFFF;
  border: 1px solid #E9F0EB;
  box-sizing: border-box;
  border-radius: 50px;
  height: 60px;
  width: 80%;
  padding-left: 20px;
  font-weight: 700;
  font-size: 24px;
  color: #283044;
}
.search:focus{
  outline: none;
}
.search::placeholder{
  font-size: 20px;
  color: #D9E4DC;
  font-weight: normal;
}
.search-btn{
  background: linear-gradient(279.56deg, #65B3E4 15.15%, rgba(120, 161, 187, 0) 171.55%);
  border-radius: 50px;
  width: 20%;
}
.image-column{
  position: relative;
  background-color: #F7F7F7;
  border-radius: 40px 0px 0px 40px;
  height: 100vh;
}
.car-img{
  position: absolute;
  z-index: 10;
}
.road-img{
  position: absolute;
  z-index: 7;
}
.peshehod{
  position: absolute;
  z-index: 8;
}
.img-title{
  position: absolute;
  z-index: 9;
}
.nav-brand{
  font-weight: 700;
}

</style>
