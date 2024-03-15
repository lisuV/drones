<script setup>
  
</script>

<template>   
  <main class="main">
    <div class="bg-img">
      <h1 class="main-text">Scalable drones & autopilots</h1>
    </div>
    
      <ul class="quick-access">
        <li class="quick-access-product-container">
          <div class="quick-access-info"> 
            <img class="quick-access-img" src="/src/icons/HomePage/quickAccessUAV.png" alt="UAV">
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
            <img class="quick-access-img" src="/src/icons/HomePage/quickAccessDrone1.png" alt="Drone 1">
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
      <h1> Benefits</h1>
    
    
  </main>
</template>

<style>
.main{
  background: #F9F9F9;
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
  height:91%;
}
.quick-access-img{
  height: auto;
  width: 95%;
}
.quick-access-category{
  color: #BBB;
  font-family: Montserrat;
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
</style>
