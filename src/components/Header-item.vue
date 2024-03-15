<script>
import droneImage from '@/icons/Drone1Pruducts.png'; // Adjust the path based on your project structure
import sribogImage from '@/icons/SribogUAVProducts.png'; // Adjust the path based on your project structure

export default {
  data() {
    return {
      isDropdownOpenProducts: false,
      isDropdownOpenLanguages: false,
      products: [
        { name: 'DroneCore 1', id: 1, img: droneImage, details: 'AI-driven autopilot with NVIDIA Jetson, Cube, and ESCs' },
        { name: 'Stribog UAV', id: 2, img: sribogImage, details: 'Multi-purpose & open-architecture development platform ready for instant deployment' },
      ],
      languages: [
        { name: 'EN', id: 1, actual: false},
        { name: 'SK', id: 2, actual: true},
        { name: 'UA', id: 3, actual: false},
      ],
      actualLanguage: "",
      selectLenguages: [],
      updateLenguages: [],
    };
  },
  created (){
    this.actualLanguage = this.displayActualLenguage();
  },
  methods: {
    openDropdownProducts() {
      this.isDropdownOpenProducts = true;
    },
    closeDropdownProducts() {
      this.isDropdownOpenProducts = false;
    },
    openDropdownLanguages() {
      this.isDropdownOpenLanguages = true;
    },
    closeDropdownLanguages() {
      this.isDropdownOpenLanguages = false;
    },
    displayActualLenguage() {
      this.selectLenguages=[];
      this.languages.forEach(leng => {
        if(leng.actual==true){
          this.actualLanguage = leng.name;
        }
        if(leng.actual==false){
          this.selectLenguages.push(leng);
        }
      });
      return this.actualLanguage;
    },
    changeActualLenguage(id){
      //var updateLenguage = [];
      this.languages.forEach(leng => {
        if(leng.id==id){
          leng.actual = true;
          this.updateLenguages.push(leng);
        }
        if(leng.id!=id){
          leng.actual = false;
          this.updateLenguages.push(leng);
        }
      });
      this.languages.lenght = this.updateLenguages;
      return this.displayActualLenguage(); 
    }
  }
};
</script>

<template>
  <!-- connect fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <!-- Michroma.Monserrat -->
    <link href="https://fonts.googleapis.com/css2?family=Michroma&family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
  <!-- connect fonts -->

  <header class="header">
    <div class="logo-container">
      <img class="logo" src="/src/icons/AIrones_logo.png" alt="Company Logo">
      <span class="company-name">AIrones s.r.o</span>
    </div>
    <nav class="nav">
      <ul class="nav-links">
        <li class="nav-item">Home</li>
        <li class="nav-item">About us</li>
        <li class="nav-item" 
        @mouseover="openDropdownProducts" 
        @mouseleave="closeDropdownProducts"> 
        <div class="productAreaName">Products</div>
          <ul v-if="isDropdownOpenProducts" class="dropdownProducts" >
            <li v-for="product in products" :key="product.id">
              <a class="productList">
                <img :src="product.img" alt="Product Image" class="productListImg">
                <div class="productListText">
                  <div class="productListName"> {{ product.name }}</div>
                  <div class="productListDetails">{{ product.details }}</div> 
                </div>
              </a>
            </li>
          </ul>  
        </li>
        <li class="nav-item">Contacts</li>
        <li class="nav-item" 
        @mouseover="openDropdownLanguages"
        @mouseleave="closeDropdownLanguages">
          <div class="actuallenguage">
            <div class="langListName">
              <div class="nameAclualLanguage">{{actualLanguage}}</div>
              <img v-if="!isDropdownOpenLanguages" src="/src/icons/languages/arrowDown.png" class="arrow">
              <img v-if="isDropdownOpenLanguages" src="/src/icons/languages/arrowUp.png" class="arrow">
            </div>
          </div>
          <ul v-if="isDropdownOpenLanguages" class="Languages">
            <li v-for="leng in selectLenguages" :key="leng.id" >
               <div class="langListName" @click="changeActualLenguage(leng.id)">{{ leng.name }}</div>
            </li>
          </ul>

        </li>
      </ul>
    </nav>
  </header>
</template>


<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 125px; /* Змінюємо висоту на відсоткове значення */
  max-width: 100%; /* Зберігаємо максимальну ширину */
  padding: 0 3%; /* Змінюємо відступи */
  background-color: #F9F9F9;
}

.logo-container {
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  gap: 16px;
}
.logo {
  min-width: 32px;
  width: 2.2%;
  height: auto;
  margin-left: 6.6%;
}
.company-name {
  color: #000;
  font-family:  "Michroma", sans-serif;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  width:auto;
  margin-right: 64px;
  white-space: nowrap;
}

.nav {
  display: flex;
  margin-right: 7%;
  width: 40%;
}
.nav-links {
  list-style: none;
  margin-left: 0;
  padding: 0;
  display: flex;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}
.nav-item {
/*margin: 5%;*/  
  padding-top:6.6px;
  text-decoration: none;
  color: #121212;
  font-family: "Montserrat", sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  height: 30px;
  text-align: center;
}
.nav-item:last-child{
  padding-top: 0px;
}

.productAreaName{
  height: 60px;
  color: #121212;
  font-family: "Montserrat", sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}
.dropdownProducts{
  color: #121212;
  border-radius: 24px;
  background: #FFF;
  font-family: "Montserrat", sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
  width: 338px;
  position: absolute;
  top: 85px; /* Position dropdown list below the header menu */
  list-style-type: none; /* Remove default bullets */
  display: flex;
  flex-wrap: nowrap;
  justify-content: space-between;
  flex-direction: column;
  padding: 0px;
  border-radius: 24px;
}
.dropdownProducts li{
  padding: 15px 20px 15px 14px;
}
.dropdownProducts li:first-child{
  border-radius: 24px 24px 0px 0px;
}
.dropdownProducts li:last-child{
  border-radius: 0px 0px 24px 24px;
}
.dropdownProducts li:hover{
  background: rgba(187, 187, 187, 0.20);
}
.productList{ 
  display: flex;
  flex-wrap: nowrap; 
  pointer-events: none; 
}
.productListImg{
  width: 83px;
  height: auto;
  align-items: left;
  margin-right: 14px;
}
.productListText{
  text-align: left;
  font-family: "Montserrat", sans-serif;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}
.productListName{
  color: #121212;
  font-size: 14px;
}
.productListDetails{
  color: #BBB;
  font-size: 12px;
}


.Languages{
  list-style-type: none; /* Remove default bullets */
  position: absolute;
  padding-left:0px;
}
.actuallenguage {
  height: 30px;
}
.arrow{
  height: auto;
  width: 14px;
}
.langListName {
  border-radius: 4px;
  background: #121212;

  display: inline-flex;
  padding: 4px 8px;
  justify-content: center;
  align-items: center;
  gap: 8px;
  
  width: 60px;
  height: 25px;
  margin: 4px;
 
  color: #FFF;
  font-family: "Montserrat", sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.nameAclualLanguage{
  display: inline-flex;
  justify-content: center;
  align-items: center;
  height: 21px;
  width: 17px;
}


</style>