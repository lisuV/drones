<script>
import drone1Image from '@/icons/HomePage/products/DroneCore1.png'; // Adjust the path based on your project structure
import sribogImage from '@/icons/HomePage/products/UAV.png'; // Adjust the path based on your project structure
import drone2Image from '@/icons/HomePage/soon/DroneCore2.png';
import dronePXImage from '@/icons/HomePage/soon/DroneCorePX.png';

export default {
  data() {
    return {
      isDropdownOpenProducts: false,
      isDropdownOpenLanguages: false,
      products: [
        { name: 'DroneCore 1', id: 1, 
        img: drone1Image, 
        detail_1: 'NVIDIA Jetson Orin NX or Jetson Xavier NX & CubePilot', 
        detail_2: '4x Electronic Speed Controllers',
        detail_3: 'Rich connectivity for different payloads'},
        { name: 'Stribog UAV', id: 2, 
        img: sribogImage,
        detail_1: 'Based on the newest DroneCore suite', 
        detail_2: 'Full MAVLink support',
        detail_3: 'SineSpine FOC ESC (up to 15% more efficiency)'},
      ],
      productsSoon: [
      { name: 'DroneCore 2', id: 1, 
        img: drone2Image, 
        details: 'DroneCore natively supported by Ardupilot', 
      },
        { name: 'DroneCore PX', id: 2, 
        img: dronePXImage,
        details: 'DroneCore compatible with Pixhawk PX4 FMU', 
        },
      ]
    };
  },
};
</script>

<template>   
  <main class="main">
    <div class="bg-img">
      <h1 class="main-text">Scalable drones & autopilots</h1>
    </div>
    
    <ul class="quick-access">
        <li class="quick-access-product-container">
          <div class="quick-access-info"> 
            <div class=".quick-access-img-block">
              <img class="quick-access-img" src="/src/icons/HomePage/quickAccessUAV.png" alt="UAV">
            </div>
                       
            <div class="quick-access-category">DRONES</div>
            <div class="quick-access-main-text">The most powerful open-architecture UAV platform on the market</div>
            <ul class="quick-access-detail-text">
              <li>Gimbal by NextVision incl. thermal cam</li>
              <li>DoodleLabs Mesh Radio</li>
              <li>60 min flight time</li>
              <li>Open architecture with Jetson Orin NX & CubePilot</li>
            </ul>
          </div>
          <div class="quick-access-buttons">
            <div class="quick-access-button-details">See details</div>
            <div class="quick-access-button-quote">Get a quote</div>
          </div>
        </li>
        <li class="quick-access-product-container">
          <div class="quick-access-info">
            <div class=".quick-access-img-block">
              <img class="quick-access-img" src="/src/icons/HomePage/quickAccessDrone1.png" alt="Drone 1">
            </div>
            <div class="quick-access-category">AUTOPILOTS</div>
            <div class="quick-access-main-text">Robust UAS autopilot combining NVIDIA Jetson and Cube / Pixhawk</div>
            <ul class="quick-access-detail-text">
              <li>Carrier board + Companion computer (Jetson Orin NX or Xavier NX)</li>
              <li>Cube Orange+ or Blue</li>
              <li>ESCs (v1)</li>
            </ul>
          </div>
          <div class="quick-access-buttons">
            <div class="quick-access-button-details">See details</div>
            <div class="quick-access-button-quote">Get a quote</div>
          </div>
        </li>
    </ul>
    <div class="benefits">
        <h1 class="main-header">Benefits</h1>
        <p class="benefits-main-details">DroneCore autopilots are one-stop solution for UAS developers combining carrier board, companion computer, rich connectivity, and ESCs (v1).</p>
               
        <div class="benefits-items">
          <div class="benefits-item">
            <img class="benefits-icon" src="/src/icons/HomePage/benefits/wallet.png">
            <p class="benefits-item-name">Cost efficiency</p>
          </div>
          <div class="benefits-item">
            <img class="benefits-icon" src="/src/icons/HomePage/benefits/rocket.png">
            <p class="benefits-item-name">Faster development</p>
          </div>
          <div class="benefits-item">
            <img class="benefits-icon" src="/src/icons/HomePage/benefits/shield.png">
            <p class="benefits-item-name">Resilience</p>
          </div>
        </div>
    </div>

    <div class="products">
      <h1 class="main-header">Products</h1>
      <ul class="products-list">
        <li v-for="product in products" :key="product.id">
          <div class="products-item">
            <div class="products-item-text">
              <div>
                <div class="products-item-name"> {{ product.name }}</div>
                <ul class="products-item-details">
                  <li>{{ product.detail_1 }}</li> 
                  <li>{{ product.detail_2 }}</li>
                  <li>{{ product.detail_3 }}</li> 
                </ul>
              </div>
              <div class="quick-access-buttons">
                <div class="quick-access-button-details">See details</div>
                <div class="quick-access-button-quote">Get a quote</div>
              </div>
            </div>
            <img :src="product.img" alt="Product Image" class="products-item-img">
          </div>
        </li>
        <li>
          <div class="products-item">
            <div class="products-item-text">
              <div>
                 <div class="products-item-name">Custom solutions</div>
              <p class="products-item-details">We develop custom hardware and software solutions for autonomous UASs</p>
              </div>
              <div class="quick-access-buttons">
                <div class="quick-access-button-quote">Get a quote</div>
              </div>
            </div>
            <img src="/src/icons/HomePage/products/custom.png" alt="Product Image" class="products-item-img custom">
          </div>
        </li>
      </ul>
    </div>

    <div class="products soon">
      <h1 class="main-header">Soon</h1>
      <ul class="products-list">
        <li v-for="product in productsSoon" :key="product.id">
          <div class="products-item soon-item">
            <div class="products-item-text">
              <div class="products-item-name"> {{ product.name }}</div>
              <p class="products-item-details soon-item-datails">{{ product.details }}</p> 
              <div class="products-soon-coming">Coming soon</div>
            </div>
            <img :src="product.img" alt="Product Image" class="products-item-img">
          </div>
        </li>
      </ul>
    </div>
    
  </main>
</template>

<style>
.main{
  background: #F9F9F9;
}
.main-header{
  color: #121212;
  font-family: "Montserrat", sans-serif;
  font-size: 48px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}
.bg-img {
  background-image: url('/src/icons/HomePage/Background Page.png');
  background-size: cover;
  background-position: center;
  height: 90vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
.main-text {
  color: #FFF;
  font-family:  "Michroma", sans-serif;
  font-size: 56px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  text-align: center;
}

.quick-access{
  margin-left: 6.6%;
  margin-right: 6.6%;
  padding: 4% 3% 1% 3%;
  gap: 2%;
  border-radius: 24px;
  background: #FFF;
  list-style-type: none; /* Remove default bullets */
  display:flex;
  justify-content: space-between;
  flex-direction: row;
  position: relative;
  top: -10vh;
}
.quick-access-product-container{
  padding-right: 10xp;
}
.quick-access-info{
  height: 91%; 
}
.quick-access-img-block{
  display: flex;
  height: auto;
  width: 100%;
  align-items: center;
  justify-content: center;
}
.quick-access-img{
  height: auto;
  width: 95%;
}
.quick-access-category{
  color: #BBB;
  font-family: "Montserrat", sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  margin-top: 12px;
  margin-bottom: 20px;

}
.quick-access-main-text{
  color: #121212;
  font-family: "Montserrat", sans-serif;
  font-size: 32px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
  margin-bottom: 25px;
}
.quick-access-detail-text{
  color: #ADADAD;
  font-family: "Montserrat", sans-serif;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  list-style-type:disc;
  padding-left: 20px;
  padding-bottom: 15%;
}
.quick-access-buttons{
  display:flex;
  justify-content:flex-start;
  flex-direction: row;
  gap: 16px;
}
.quick-access-button-details{
  display: inline-flex;
  padding: 14px 18px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 8px;
  background: #121212;
  color: #FFF;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}
.quick-access-button-quote{
  display: inline-flex;
  padding: 14px 18px;
  justify-content: center;
  align-items: center;
  gap: 10px;
  border-radius: 8px;
  border: 1px solid #121212;
  color: #121212;
  font-family: Montserrat;
  font-size: 16px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.benefits{
  display:flex;
  flex-direction: column;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 100px;
}
.benefits-main-details{
  color: #ADADAD;
  text-align: center;
  font-family: "Montserrat", sans-serif;
  font-size: 22px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;

  margin-block-start: 1.2rem;
  margin-left: 12%;
  margin-right: 12%;
  margin-block-end: 0;
}
.benefits-items{
  display:flex;
  gap: 7%;
  align-items: start;
  padding-top: 80px;
  width: -webkit-fill-available;
  flex-direction: row;
  flex-wrap: wrap;
  margin-block-start: 1.2rem;
  justify-content: center;
}
.benefits-item{
  gap: 32px;
  align-items: center;
  text-align: center;
  display: flex;
  width: 22%;
  flex-direction: column;
  align-items: center;
}
.benefits-item-name{
  color: #121212;
  font-family: "Montserrat", sans-serif;
  font-size: 30px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  width: max-content;
  word-wrap: break-word;
}
.benefits-icon{
  width:50px;
  height: 50px;
}

.products{
  display:flex;
  flex-direction: column;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 190px;
}
.products-list{
  display:flex;
  flex-direction: column;
  margin-left: 6.6%;
  margin-right: 6.6%;
  list-style-type: none;
  margin-top: 50px;
  width: -webkit-fill-available;
  gap: 30px;
}
.products-item{
  flex-shrink: 0;
  border-radius: 24px;
  background: #FFF;
  display:flex;
  flex-direction: row;
  flex-wrap: wrap;
  justify-content: space-between;
  padding-top: 45px;
  padding-bottom: 45px;
  padding-right: 2.5%;
}
.products-item-text{
  display:flex;
  flex-direction: column;
  justify-content: space-between;
  padding-top: 35px;
  padding-left: 7.6%;
  margin-bottom: 35px;
  max-width: 60%;
}
.products-item-name{
  color: #121212;
  font-family: "Montserrat", sans-serif;
  font-size: 40px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}
.products-item-details{
  color: #ADADAD;
  font-family: "Montserrat", sans-serif;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  list-style-type:disc;
  margin-bottom: 56px;
  padding-top: 25px;
  word-wrap: break-word !important;
}
.products-item-img{
  width: 40%;
  height: auto;
}
.custom{
  width: 35%;
  height: auto;
  padding-right: 5%;
}

.soon-item{
  align-items: center;
}

.soon-item-datails{
  margin-bottom: 24px;
}
.products-soon-coming{
  color: #121212;
  font-family: Montserrat;
  font-size: 20px;
  font-style: normal;
  font-weight: 600;
  line-height: normal;
}

</style>
